---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 8c1369cdedf8848f3c62ca6b6bc4eb3d2d78be95
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/28/2019
ms.locfileid: "74656820"
---
## <a name="280---october-2019"></a><span data-ttu-id="41d91-103">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="41d91-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="41d91-104">一般</span><span class="sxs-lookup"><span data-stu-id="41d91-104">General</span></span>
* <span data-ttu-id="41d91-105">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="41d91-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="41d91-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-106">Az.Accounts</span></span>
* <span data-ttu-id="41d91-107">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="41d91-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="41d91-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-108">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-109">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="41d91-110">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-111">Az.Automation</span></span>
* <span data-ttu-id="41d91-112">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="41d91-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="41d91-113">Az.Batch</span></span>
* <span data-ttu-id="41d91-114">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="41d91-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-115">Az.Compute</span></span>
* <span data-ttu-id="41d91-116">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="41d91-117">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="41d91-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="41d91-118">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="41d91-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="41d91-119">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="41d91-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-120">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-121">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="41d91-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="41d91-122">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="41d91-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="41d91-123">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="41d91-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-125">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="41d91-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="41d91-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="41d91-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="41d91-127">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="41d91-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="41d91-128">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="41d91-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="41d91-129">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="41d91-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="41d91-130">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="41d91-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-131">Az.IotHub</span></span>
* <span data-ttu-id="41d91-132">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="41d91-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="41d91-133">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="41d91-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="41d91-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-134">Az.Monitor</span></span>
* <span data-ttu-id="41d91-135">已針對 New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver 新增了新的動作群組接收器</span><span class="sxs-lookup"><span data-stu-id="41d91-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="41d91-136">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="41d91-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="41d91-137">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="41d91-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="41d91-138">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="41d91-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-139">Az.Network</span></span>
* <span data-ttu-id="41d91-140">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="41d91-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="41d91-141">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="41d91-142">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-142">New cmdlets added:</span></span>
        - <span data-ttu-id="41d91-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="41d91-144">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzVirtualNetworkGatewayConnection   -Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="41d91-145">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-145">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="41d91-146">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-146">Updated cmdlets:</span></span>
        - <span data-ttu-id="41d91-147">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-147">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="41d91-148">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-148">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="41d91-149">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-149">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="41d91-150">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="41d91-150">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="41d91-151">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="41d91-151">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="41d91-152">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="41d91-152">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="41d91-153">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="41d91-153">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="41d91-154">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="41d91-154">Az.RedisCache</span></span>
* <span data-ttu-id="41d91-155">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="41d91-155">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-156">Az.Sql</span></span>
* <span data-ttu-id="41d91-157">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-157">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-158">Az.Storage</span></span>
* <span data-ttu-id="41d91-159">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="41d91-159">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="41d91-160">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="41d91-160">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="41d91-161">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="41d91-161">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="41d91-162">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="41d91-162">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="41d91-163">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-163">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="41d91-164">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="41d91-164">Az.StorageSync</span></span>
* <span data-ttu-id="41d91-165">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="41d91-165">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-166">Az.Websites</span></span>
* <span data-ttu-id="41d91-167">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="41d91-167">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="41d91-168">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="41d91-168">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="41d91-169">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-169">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-170">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="41d91-170">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="41d91-171">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="41d91-171">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="41d91-172">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="41d91-172">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-173">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-173">Az.Automation</span></span>
* <span data-ttu-id="41d91-174">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="41d91-174">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="41d91-175">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="41d91-175">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="41d91-176">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="41d91-176">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-177">Az.Compute</span></span>
* <span data-ttu-id="41d91-178">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-178">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="41d91-179">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="41d91-179">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="41d91-180">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="41d91-180">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="41d91-181">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="41d91-181">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="41d91-182">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="41d91-182">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="41d91-183">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="41d91-183">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="41d91-184">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="41d91-184">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="41d91-185">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="41d91-185">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="41d91-186">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-186">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-187">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-187">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-188">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="41d91-188">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="41d91-189">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="41d91-189">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="41d91-190">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="41d91-190">Az.HDInsight</span></span>
* <span data-ttu-id="41d91-191">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="41d91-191">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-192">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-192">Az.IotHub</span></span>
* <span data-ttu-id="41d91-193">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-193">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="41d91-194">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-194">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="41d91-195">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="41d91-195">New cmdlets are:</span></span>
    - <span data-ttu-id="41d91-196">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="41d91-196">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="41d91-197">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="41d91-197">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="41d91-198">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="41d91-198">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="41d91-199">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="41d91-199">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-200">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-200">Az.Monitor</span></span>
* <span data-ttu-id="41d91-201">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="41d91-201">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="41d91-202">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="41d91-202">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="41d91-203">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="41d91-203">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="41d91-204">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="41d91-204">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="41d91-205">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="41d91-205">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="41d91-206">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="41d91-206">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="41d91-207">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="41d91-207">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="41d91-208">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="41d91-208">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="41d91-209">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="41d91-209">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="41d91-210">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="41d91-210">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="41d91-211">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="41d91-211">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="41d91-212">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="41d91-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="41d91-213">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="41d91-213">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="41d91-214">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="41d91-214">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="41d91-215">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="41d91-215">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="41d91-216">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="41d91-216">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="41d91-217">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="41d91-217">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="41d91-218">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-218">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="41d91-219">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-219">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="41d91-220">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="41d91-220">Overall improved help files</span></span>
* <span data-ttu-id="41d91-221">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="41d91-221">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-222">Az.Network</span></span>
* <span data-ttu-id="41d91-223">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-223">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="41d91-224">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="41d91-224">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="41d91-225">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="41d91-225">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="41d91-226">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="41d91-226">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="41d91-227">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="41d91-227">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="41d91-228">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="41d91-228">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="41d91-229">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="41d91-229">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="41d91-230">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="41d91-230">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="41d91-231">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="41d91-231">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="41d91-232">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="41d91-232">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="41d91-233">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="41d91-233">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="41d91-234">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="41d91-234">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="41d91-235">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-235">New cmdlets</span></span>
        - <span data-ttu-id="41d91-236">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="41d91-236">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="41d91-237">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-237">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="41d91-238">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-238">Updated cmdlet:</span></span>
        - <span data-ttu-id="41d91-239">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="41d91-239">New-VpnSite</span></span>
        - <span data-ttu-id="41d91-240">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="41d91-240">Update-VpnSite</span></span>
        - <span data-ttu-id="41d91-241">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-241">New-VpnConnection</span></span>
        - <span data-ttu-id="41d91-242">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-242">Update-VpnConnection</span></span>
* <span data-ttu-id="41d91-243">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-243">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-244">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-244">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-245">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="41d91-245">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="41d91-246">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="41d91-246">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-247">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-247">Az.Resources</span></span>
* <span data-ttu-id="41d91-248">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="41d91-248">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-249">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-249">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-250">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-250">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="41d91-251">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="41d91-251">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="41d91-252">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41d91-252">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="41d91-253">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41d91-253">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="41d91-254">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41d91-254">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="41d91-255">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="41d91-255">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="41d91-256">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41d91-256">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="41d91-257">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41d91-257">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="41d91-258">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41d91-258">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="41d91-259">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41d91-259">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="41d91-260">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="41d91-260">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="41d91-261">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="41d91-261">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="41d91-262">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="41d91-262">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="41d91-263">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41d91-263">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="41d91-264">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="41d91-264">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="41d91-265">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="41d91-265">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="41d91-266">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="41d91-266">Az.SignalR</span></span>
* <span data-ttu-id="41d91-267">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-267">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-268">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-268">Az.Sql</span></span>
* <span data-ttu-id="41d91-269">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-269">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="41d91-270">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="41d91-270">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="41d91-271">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="41d91-271">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="41d91-272">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="41d91-272">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="41d91-273">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="41d91-273">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-274">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-274">Az.Storage</span></span>
* <span data-ttu-id="41d91-275">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-275">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="41d91-276">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="41d91-276">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="41d91-277">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41d91-277">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="41d91-278">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41d91-278">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="41d91-279">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-279">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="41d91-280">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41d91-280">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="41d91-281">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="41d91-281">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="41d91-282">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="41d91-282">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="41d91-283">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="41d91-283">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="41d91-284">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="41d91-284">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="41d91-285">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="41d91-285">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-286">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-286">Az.Websites</span></span>
* <span data-ttu-id="41d91-287">修正了將應用程式遷移到新的 ASP 時，webapp 標籤遭到刪除的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-287">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="41d91-288">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="41d91-288">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="41d91-289">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-289">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="41d91-290">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="41d91-290">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="41d91-291">一般</span><span class="sxs-lookup"><span data-stu-id="41d91-291">General</span></span>
* <span data-ttu-id="41d91-292">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="41d91-292">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="41d91-293">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-293">Az.Accounts</span></span>
* <span data-ttu-id="41d91-294">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="41d91-294">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="41d91-295">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="41d91-295">Az.Aks</span></span>
* <span data-ttu-id="41d91-296">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="41d91-296">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="41d91-297">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="41d91-297">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="41d91-298">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-298">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-299">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-299">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="41d91-300">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="41d91-300">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="41d91-301">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-301">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="41d91-302">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="41d91-302">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="41d91-303">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="41d91-303">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="41d91-304">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="41d91-304">Az.Batch</span></span>
* <span data-ttu-id="41d91-305">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="41d91-305">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="41d91-306">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="41d91-306">Az.Cdn</span></span>
* <span data-ttu-id="41d91-307">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-307">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-308">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-308">Az.Compute</span></span>
* <span data-ttu-id="41d91-309">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-309">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="41d91-310">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="41d91-310">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="41d91-311">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="41d91-311">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="41d91-312">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="41d91-312">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="41d91-313">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="41d91-313">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="41d91-314">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="41d91-314">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="41d91-315">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-315">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="41d91-316">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="41d91-316">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-317">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-317">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-318">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="41d91-318">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="41d91-319">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="41d91-319">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="41d91-320">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="41d91-320">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="41d91-321">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="41d91-321">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-322">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-322">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-323">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="41d91-323">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="41d91-324">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="41d91-324">Az.EventHub</span></span>
* <span data-ttu-id="41d91-325">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="41d91-325">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="41d91-326">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="41d91-326">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="41d91-327">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-327">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="41d91-328">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="41d91-328">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="41d91-329">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="41d91-329">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="41d91-330">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="41d91-330">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-331">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-331">Az.Monitor</span></span>
* <span data-ttu-id="41d91-332">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-332">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-333">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-333">Az.Network</span></span>
* <span data-ttu-id="41d91-334">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-334">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="41d91-335">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-335">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="41d91-336">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="41d91-336">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="41d91-337">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-337">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="41d91-338">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="41d91-338">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="41d91-339">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="41d91-339">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="41d91-340">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="41d91-340">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-341">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-341">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-342">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="41d91-342">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="41d91-343">新增了範例</span><span class="sxs-lookup"><span data-stu-id="41d91-343">Added example</span></span>
    - <span data-ttu-id="41d91-344">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="41d91-344">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="41d91-345">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-345">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="41d91-346">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="41d91-346">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-347">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-348">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-348">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-349">Az.Resources</span></span>
* <span data-ttu-id="41d91-350">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-350">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="41d91-351">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-351">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="41d91-352">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="41d91-352">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="41d91-353">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="41d91-353">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-354">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-355">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-355">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="41d91-356">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="41d91-356">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="41d91-357">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="41d91-357">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-358">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-359">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="41d91-359">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="41d91-360">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="41d91-360">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="41d91-361">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="41d91-361">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="41d91-362">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="41d91-362">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="41d91-363">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="41d91-363">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="41d91-364">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-364">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-365">Az.Sql</span></span>
* <span data-ttu-id="41d91-366">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="41d91-366">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-367">Az.Storage</span></span>
* <span data-ttu-id="41d91-368">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="41d91-368">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="41d91-369">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="41d91-369">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="41d91-370">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41d91-370">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="41d91-371">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="41d91-371">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="41d91-372">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="41d91-372">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="41d91-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="41d91-373">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-374">Az.Websites</span></span>
* <span data-ttu-id="41d91-375">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="41d91-375">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="41d91-376">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="41d91-376">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-377">Az.Accounts</span></span>
* <span data-ttu-id="41d91-378">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="41d91-378">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="41d91-379">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-379">Az.ApplicationInsights</span></span>
* <span data-ttu-id="41d91-380">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-380">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="41d91-381">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-381">Az.Automation</span></span>
* <span data-ttu-id="41d91-382">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-382">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-383">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-384">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-384">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-385">Az.Compute</span></span>
* <span data-ttu-id="41d91-386">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="41d91-386">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="41d91-387">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41d91-387">Az.ContainerRegistry</span></span>
* <span data-ttu-id="41d91-388">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-388">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="41d91-389">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="41d91-389">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-390">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-390">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-391">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="41d91-391">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="41d91-392">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-392">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="41d91-393">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="41d91-393">Az.EventHub</span></span>
* <span data-ttu-id="41d91-394">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="41d91-394">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="41d91-395">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-395">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="41d91-396">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-396">Az.KeyVault</span></span>
* <span data-ttu-id="41d91-397">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-397">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="41d91-398">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="41d91-398">Az.LogicApp</span></span>
* <span data-ttu-id="41d91-399">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="41d91-399">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="41d91-400">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-400">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="41d91-401">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="41d91-401">Az.ManagedServices</span></span>
* <span data-ttu-id="41d91-402">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-402">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-403">Az.Network</span></span>
* <span data-ttu-id="41d91-404">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-404">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="41d91-405">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-405">New cmdlets</span></span>
        - <span data-ttu-id="41d91-406">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="41d91-406">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="41d91-407">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-407">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="41d91-408">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-408">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="41d91-409">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-409">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="41d91-410">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-410">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="41d91-411">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-411">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="41d91-412">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="41d91-412">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="41d91-413">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-413">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="41d91-414">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="41d91-414">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="41d91-415">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-415">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="41d91-416">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="41d91-416">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="41d91-417">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="41d91-417">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="41d91-418">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="41d91-418">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="41d91-419">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="41d91-419">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="41d91-420">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-420">Updated cmdlets</span></span>
        - <span data-ttu-id="41d91-421">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-421">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="41d91-422">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-422">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="41d91-423">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-423">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="41d91-424">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="41d91-424">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="41d91-425">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="41d91-425">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="41d91-426">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-426">Updated cmdlet:</span></span>
        - <span data-ttu-id="41d91-427">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-427">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="41d91-428">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-428">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="41d91-429">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-429">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="41d91-430">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="41d91-430">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="41d91-431">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="41d91-431">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="41d91-432">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="41d91-432">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-433">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-433">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-434">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="41d91-434">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="41d91-435">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="41d91-435">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-436">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-437">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-437">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="41d91-438">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-438">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="41d91-439">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-439">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="41d91-440">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-440">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="41d91-441">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-441">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="41d91-442">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-442">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="41d91-443">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-443">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="41d91-444">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-444">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="41d91-445">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="41d91-445">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="41d91-446">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="41d91-446">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-447">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-447">Az.Resources</span></span>
- <span data-ttu-id="41d91-448">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-448">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="41d91-449">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="41d91-449">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-450">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-450">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-451">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="41d91-451">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="41d91-452">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-452">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-453">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-453">Az.Sql</span></span>
* <span data-ttu-id="41d91-454">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-454">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="41d91-455">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-455">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="41d91-456">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="41d91-456">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-457">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-457">Az.Storage</span></span>
* <span data-ttu-id="41d91-458">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-458">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="41d91-459">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="41d91-459">Az.StorageSync</span></span>
* <span data-ttu-id="41d91-460">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-460">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="41d91-461">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="41d91-461">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-462">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-462">Az.Websites</span></span>
* <span data-ttu-id="41d91-463">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="41d91-463">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="41d91-464">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="41d91-464">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="41d91-465">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="41d91-465">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="41d91-466">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="41d91-466">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-467">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-467">Az.Accounts</span></span>
* <span data-ttu-id="41d91-468">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-468">Add support for profile cmdlets</span></span>
* <span data-ttu-id="41d91-469">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-469">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="41d91-470">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-470">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="41d91-471">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="41d91-471">Az.Advisor</span></span>
* <span data-ttu-id="41d91-472">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="41d91-472">GA release of Az.Advisor</span></span>
* <span data-ttu-id="41d91-473">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="41d91-473">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="41d91-474">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-474">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-475">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-475">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="41d91-476">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="41d91-476">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="41d91-477">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-477">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="41d91-478">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-478">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="41d91-479">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-479">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="41d91-480">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="41d91-480">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="41d91-481">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-481">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-482">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-482">Az.Automation</span></span>
* <span data-ttu-id="41d91-483">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="41d91-483">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-484">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-484">Az.Compute</span></span>
* <span data-ttu-id="41d91-485">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-485">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-486">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-487">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="41d91-487">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="41d91-488">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="41d91-488">Az.EventGrid</span></span>
* <span data-ttu-id="41d91-489">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-489">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-490">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-490">Az.IotHub</span></span>
* <span data-ttu-id="41d91-491">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-491">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-492">Az.Network</span></span>
* <span data-ttu-id="41d91-493">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="41d91-493">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="41d91-494">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-494">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="41d91-495">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-495">Az.PolicyInsights</span></span>
* <span data-ttu-id="41d91-496">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="41d91-496">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="41d91-497">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="41d91-497">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-498">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-498">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-499">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="41d91-499">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-500">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-501">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="41d91-501">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-502">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-502">Az.Resources</span></span>
    - <span data-ttu-id="41d91-503">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="41d91-503">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="41d91-504">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="41d91-504">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="41d91-505">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="41d91-505">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="41d91-506">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="41d91-506">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-507">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-507">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-508">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="41d91-508">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-509">Az.Sql</span></span>
* <span data-ttu-id="41d91-510">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="41d91-510">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="41d91-511">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="41d91-511">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="41d91-512">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-512">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="41d91-513">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-513">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="41d91-514">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-514">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="41d91-515">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-515">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="41d91-516">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-516">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="41d91-517">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="41d91-517">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="41d91-518">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="41d91-518">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-519">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-519">Az.Storage</span></span>
* <span data-ttu-id="41d91-520">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="41d91-520">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="41d91-521">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="41d91-521">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="41d91-522">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="41d91-522">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="41d91-523">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="41d91-523">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="41d91-524">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="41d91-524">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="41d91-525">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-525">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="41d91-526">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-526">Set-AzStorageAccount</span></span>
* <span data-ttu-id="41d91-527">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="41d91-527">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="41d91-528">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="41d91-528">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="41d91-529">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="41d91-529">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="41d91-530">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="41d91-530">Az.StorageSync</span></span>
* <span data-ttu-id="41d91-531">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="41d91-531">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="41d91-532">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="41d91-532">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-533">Az.Accounts</span></span>
* <span data-ttu-id="41d91-534">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="41d91-534">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="41d91-535">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="41d91-535">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="41d91-536">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="41d91-536">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="41d91-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="41d91-537">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="41d91-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="41d91-538">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-539">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-539">Az.Compute</span></span>
* <span data-ttu-id="41d91-540">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-540">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="41d91-541">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-541">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="41d91-542">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="41d91-542">Az.Dns</span></span>
* <span data-ttu-id="41d91-543">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="41d91-543">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="41d91-544">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="41d91-544">Az.EventGrid</span></span>
* <span data-ttu-id="41d91-545">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="41d91-545">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="41d91-546">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-546">New cmdlets:</span></span>
    - <span data-ttu-id="41d91-547">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="41d91-547">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="41d91-548">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="41d91-548">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="41d91-549">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="41d91-549">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="41d91-550">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="41d91-550">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="41d91-551">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="41d91-551">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="41d91-552">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="41d91-552">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="41d91-553">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="41d91-553">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="41d91-554">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="41d91-554">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="41d91-555">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="41d91-555">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="41d91-556">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="41d91-556">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="41d91-557">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="41d91-557">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="41d91-558">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="41d91-558">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="41d91-559">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="41d91-559">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="41d91-560">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="41d91-560">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="41d91-561">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="41d91-561">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="41d91-562">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="41d91-562">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="41d91-563">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-563">Updated cmdlets:</span></span>
    - <span data-ttu-id="41d91-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="41d91-564">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="41d91-565">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="41d91-565">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="41d91-566">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="41d91-566">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="41d91-567">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="41d91-567">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="41d91-568">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="41d91-568">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="41d91-569">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="41d91-569">Event subscription expiration date,</span></span>
            - <span data-ttu-id="41d91-570">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-570">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="41d91-571">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="41d91-571">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="41d91-572">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="41d91-572">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="41d91-573">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="41d91-573">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="41d91-574">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="41d91-574">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="41d91-575">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="41d91-575">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="41d91-576">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="41d91-576">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="41d91-577">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="41d91-577">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="41d91-578">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="41d91-578">Az.FrontDoor</span></span>
* <span data-ttu-id="41d91-579">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="41d91-579">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="41d91-580">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="41d91-580">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="41d91-581">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="41d91-581">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="41d91-582">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="41d91-582">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-583">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-583">Az.Network</span></span>
* <span data-ttu-id="41d91-584">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-584">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="41d91-585">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-585">New cmdlets</span></span>
        - <span data-ttu-id="41d91-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="41d91-586">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="41d91-587">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="41d91-587">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="41d91-588">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-588">New cmdlets</span></span> 
        - <span data-ttu-id="41d91-589">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="41d91-589">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="41d91-590">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-590">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="41d91-591">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-591">New cmdlets</span></span> 
        - <span data-ttu-id="41d91-592">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-592">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="41d91-593">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-593">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="41d91-594">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="41d91-594">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="41d91-595">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-595">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="41d91-596">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-596">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="41d91-597">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="41d91-597">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="41d91-598">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-598">New cmdlets</span></span>
        - <span data-ttu-id="41d91-599">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="41d91-599">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="41d91-600">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="41d91-600">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="41d91-601">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="41d91-601">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="41d91-602">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="41d91-602">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="41d91-603">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="41d91-603">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="41d91-604">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="41d91-604">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="41d91-605">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="41d91-605">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="41d91-606">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="41d91-606">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="41d91-607">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="41d91-607">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="41d91-608">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="41d91-608">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="41d91-609">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="41d91-609">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="41d91-610">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="41d91-610">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="41d91-611">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-611">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="41d91-612">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="41d91-612">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="41d91-613">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="41d91-613">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="41d91-614">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-614">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="41d91-615">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="41d91-615">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="41d91-616">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-616">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="41d91-617">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-617">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="41d91-618">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="41d91-618">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="41d91-619">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="41d91-619">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="41d91-620">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="41d91-620">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="41d91-621">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="41d91-621">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="41d91-622">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="41d91-622">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="41d91-623">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="41d91-623">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="41d91-624">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="41d91-624">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="41d91-625">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="41d91-625">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-626">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-626">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-627">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="41d91-627">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-628">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-628">Az.Resources</span></span>
* <span data-ttu-id="41d91-629">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="41d91-629">Support for additional Template Export options</span></span>
    - <span data-ttu-id="41d91-630">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41d91-630">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="41d91-631">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="41d91-631">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="41d91-632">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="41d91-632">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-633">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-633">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-634">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-634">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-635">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-635">Az.Sql</span></span>
* <span data-ttu-id="41d91-636">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="41d91-636">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="41d91-637">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="41d91-637">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="41d91-638">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="41d91-638">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="41d91-639">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="41d91-639">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="41d91-640">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="41d91-640">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="41d91-641">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="41d91-641">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="41d91-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="41d91-642">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="41d91-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="41d91-643">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-644">Az.Storage</span></span>
* <span data-ttu-id="41d91-645">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="41d91-645">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="41d91-646">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-646">New-AzStorageAccount</span></span>
* <span data-ttu-id="41d91-647">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="41d91-647">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="41d91-648">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-648">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-649">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-649">Az.Websites</span></span>
* <span data-ttu-id="41d91-650">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="41d91-650">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="41d91-651">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="41d91-651">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="41d91-652">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="41d91-652">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="41d91-653">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="41d91-653">Az.Cdn</span></span>
* <span data-ttu-id="41d91-654">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="41d91-654">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-655">Az.Compute</span></span>
* <span data-ttu-id="41d91-656">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="41d91-656">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="41d91-657">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="41d91-657">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="41d91-658">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="41d91-658">Az.EventHub</span></span>
* <span data-ttu-id="41d91-659">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="41d91-659">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="41d91-660">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d91-660">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-661">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-661">Az.Network</span></span>
* <span data-ttu-id="41d91-662">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="41d91-662">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="41d91-663">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="41d91-663">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="41d91-664">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-664">Az.PolicyInsights</span></span>
* <span data-ttu-id="41d91-665">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="41d91-665">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-666">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-666">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-667">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="41d91-667">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-668">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-668">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-669">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d91-669">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-670">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-670">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-671">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-671">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="41d91-672">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="41d91-672">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-673">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-673">Az.Sql</span></span>
* <span data-ttu-id="41d91-674">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="41d91-674">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="41d91-675">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-675">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="41d91-676">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="41d91-676">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="41d91-677">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-677">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-678">Az.Websites</span></span>
* <span data-ttu-id="41d91-679">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-679">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="41d91-680">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="41d91-680">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="41d91-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-681">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-682">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="41d91-682">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="41d91-683">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="41d91-683">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="41d91-684">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="41d91-684">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="41d91-685">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="41d91-685">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="41d91-686">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="41d91-686">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="41d91-687">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="41d91-687">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="41d91-688">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="41d91-688">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="41d91-689">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="41d91-689">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="41d91-690">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="41d91-690">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="41d91-691">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="41d91-691">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="41d91-692">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="41d91-692">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="41d91-693">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="41d91-693">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="41d91-694">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="41d91-694">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="41d91-695">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="41d91-695">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="41d91-696">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="41d91-696">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="41d91-697">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="41d91-697">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="41d91-698">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="41d91-698">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="41d91-699">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="41d91-699">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="41d91-700">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="41d91-700">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="41d91-701">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="41d91-701">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="41d91-702">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="41d91-702">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="41d91-703">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="41d91-703">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="41d91-704">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="41d91-704">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="41d91-705">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="41d91-705">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="41d91-706">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-706">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="41d91-707">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-707">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="41d91-708">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="41d91-708">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="41d91-709">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="41d91-709">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="41d91-710">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-710">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="41d91-711">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="41d91-711">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="41d91-712">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-712">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="41d91-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="41d91-713">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="41d91-714">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="41d91-714">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="41d91-715">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="41d91-715">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="41d91-716">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="41d91-716">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="41d91-717">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="41d91-717">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="41d91-718">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="41d91-718">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="41d91-719">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="41d91-719">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="41d91-720">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="41d91-720">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="41d91-721">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="41d91-721">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="41d91-722">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="41d91-722">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="41d91-723">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="41d91-723">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="41d91-724">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="41d91-724">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="41d91-725">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="41d91-725">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="41d91-726">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="41d91-726">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="41d91-727">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="41d91-727">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="41d91-728">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="41d91-728">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="41d91-729">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="41d91-729">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="41d91-730">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="41d91-730">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="41d91-731">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="41d91-731">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="41d91-732">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="41d91-732">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="41d91-733">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="41d91-733">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="41d91-734">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="41d91-734">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="41d91-735">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="41d91-735">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="41d91-736">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="41d91-736">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="41d91-737">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="41d91-737">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="41d91-738">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="41d91-738">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="41d91-739">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="41d91-739">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="41d91-740">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="41d91-740">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="41d91-741">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-741">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="41d91-742">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="41d91-742">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="41d91-743">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="41d91-743">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="41d91-744">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="41d91-744">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="41d91-745">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-745">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="41d91-746">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="41d91-746">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="41d91-747">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="41d91-747">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="41d91-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="41d91-748">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="41d91-749">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="41d91-749">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="41d91-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="41d91-750">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="41d91-751">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="41d91-751">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="41d91-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="41d91-752">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="41d91-753">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="41d91-753">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="41d91-754">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="41d91-754">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="41d91-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="41d91-755">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="41d91-756">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="41d91-756">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="41d91-757">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="41d91-757">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="41d91-758">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="41d91-758">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-759">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-759">Az.Automation</span></span>
* <span data-ttu-id="41d91-760">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="41d91-760">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="41d91-761">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-761">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="41d91-762">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-762">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="41d91-763">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="41d91-763">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="41d91-764">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="41d91-765">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-765">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="41d91-766">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="41d91-766">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-767">Az.Compute</span></span>
* <span data-ttu-id="41d91-768">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-768">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="41d91-769">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="41d91-769">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-770">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-770">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-771">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="41d91-771">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-772">Az.Monitor</span></span>
* <span data-ttu-id="41d91-773">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-773">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-774">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-774">Az.Network</span></span>
* <span data-ttu-id="41d91-775">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="41d91-775">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="41d91-776">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-776">Updated cmdlet:</span></span>
        - <span data-ttu-id="41d91-777">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="41d91-777">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="41d91-778">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="41d91-778">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-779">Az.Resources</span></span>
* <span data-ttu-id="41d91-780">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="41d91-780">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-781">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-781">Az.Sql</span></span>
* <span data-ttu-id="41d91-782">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="41d91-782">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="41d91-783">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="41d91-783">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-784">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-784">Az.Accounts</span></span>
* <span data-ttu-id="41d91-785">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="41d91-785">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-786">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-786">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-787">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="41d91-787">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="41d91-788">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="41d91-788">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-789">Az.Compute</span></span>
* <span data-ttu-id="41d91-790">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="41d91-790">Proximity placement group feature.</span></span>
    - <span data-ttu-id="41d91-791">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="41d91-791">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="41d91-792">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-792">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="41d91-793">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="41d91-793">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="41d91-794">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="41d91-794">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="41d91-795">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="41d91-795">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="41d91-796">重大變更</span><span class="sxs-lookup"><span data-stu-id="41d91-796">Breaking changes</span></span>
    - <span data-ttu-id="41d91-797">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="41d91-797">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="41d91-798">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="41d91-798">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="41d91-799">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="41d91-799">Az.DeploymentManager</span></span>
* <span data-ttu-id="41d91-800">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-800">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="41d91-801">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="41d91-801">Az.Dns</span></span>
* <span data-ttu-id="41d91-802">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="41d91-802">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="41d91-803">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-803">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="41d91-804">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="41d91-804">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="41d91-805">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="41d91-805">Az.FrontDoor</span></span>
* <span data-ttu-id="41d91-806">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-806">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="41d91-807">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="41d91-807">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="41d91-808">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="41d91-808">Az.HDInsight</span></span>
* <span data-ttu-id="41d91-809">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-809">Removed two cmdlets:</span></span>
    - <span data-ttu-id="41d91-810">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="41d91-810">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="41d91-811">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="41d91-811">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="41d91-812">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="41d91-812">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="41d91-813">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="41d91-813">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="41d91-814">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="41d91-814">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="41d91-815">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="41d91-815">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-816">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-816">Az.Monitor</span></span>
* <span data-ttu-id="41d91-817">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="41d91-817">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="41d91-818">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="41d91-818">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="41d91-819">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="41d91-819">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="41d91-820">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="41d91-820">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="41d91-821">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="41d91-821">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="41d91-822">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="41d91-822">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="41d91-823">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="41d91-823">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="41d91-824">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="41d91-824">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="41d91-825">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="41d91-825">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="41d91-826">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="41d91-826">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="41d91-827">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="41d91-827">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="41d91-828">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="41d91-828">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="41d91-829">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="41d91-829">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="41d91-830">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-830">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-831">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-831">Az.Network</span></span>
* <span data-ttu-id="41d91-832">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-832">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="41d91-833">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-833">New cmdlets</span></span>
        - <span data-ttu-id="41d91-834">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41d91-834">New-AzNatGateway</span></span>
        - <span data-ttu-id="41d91-835">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41d91-835">Get-AzNatGateway</span></span>
        - <span data-ttu-id="41d91-836">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41d91-836">Set-AzNatGateway</span></span>
        - <span data-ttu-id="41d91-837">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="41d91-837">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="41d91-838">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-838">Updated cmdlets</span></span>
        - <span data-ttu-id="41d91-839">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="41d91-839">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="41d91-840">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="41d91-840">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="41d91-841">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="41d91-841">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="41d91-842">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="41d91-842">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="41d91-843">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="41d91-843">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="41d91-844">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-844">Az.PolicyInsights</span></span>
* <span data-ttu-id="41d91-845">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41d91-845">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="41d91-846">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="41d91-846">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="41d91-847">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="41d91-847">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-848">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-848">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-849">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="41d91-849">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="41d91-850">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="41d91-850">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="41d91-851">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="41d91-851">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="41d91-852">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="41d91-852">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="41d91-853">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="41d91-853">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="41d91-854">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="41d91-854">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="41d91-855">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="41d91-855">Az.Relay</span></span>
* <span data-ttu-id="41d91-856">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-856">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-857">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-857">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-858">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-858">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-859">Az.Storage</span></span>
* <span data-ttu-id="41d91-860">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="41d91-860">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="41d91-861">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="41d91-861">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="41d91-862">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="41d91-862">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="41d91-863">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-863">New-AzStorageAccount</span></span>
* <span data-ttu-id="41d91-864">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="41d91-864">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="41d91-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-865">New-AzStorageAccount</span></span>
    - <span data-ttu-id="41d91-866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-866">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="41d91-867">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-867">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-868">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-868">Az.Websites</span></span>
* <span data-ttu-id="41d91-869">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="41d91-869">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="41d91-870">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="41d91-870">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="41d91-871">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="41d91-871">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="41d91-872">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="41d91-872">Highlights since the last major release</span></span>
* <span data-ttu-id="41d91-873">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="41d91-873">General availability of `Az` module</span></span>
* <span data-ttu-id="41d91-874">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="41d91-874">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="41d91-875">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="41d91-875">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="41d91-876">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-876">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="41d91-877">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="41d91-877">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="41d91-878">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-878">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="41d91-879">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-879">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="41d91-880">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-880">Az.Accounts</span></span>
* <span data-ttu-id="41d91-881">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="41d91-881">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="41d91-882">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="41d91-882">Az.Batch</span></span>
* <span data-ttu-id="41d91-883">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-883">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="41d91-884">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="41d91-884">Az.Cdn</span></span>
* <span data-ttu-id="41d91-885">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-886">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-886">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-887">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-888">Az.Compute</span></span>
* <span data-ttu-id="41d91-889">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="41d91-889">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="41d91-890">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-891">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="41d91-891">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-892">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-892">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-893">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="41d91-893">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-895">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-895">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="41d91-896">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="41d91-896">Az.EventGrid</span></span>
* <span data-ttu-id="41d91-897">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-897">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="41d91-898">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="41d91-898">Az.EventHub</span></span>
* <span data-ttu-id="41d91-899">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-899">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="41d91-900">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="41d91-900">Az.HDInsight</span></span>
* <span data-ttu-id="41d91-901">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-901">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-902">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-902">Az.IotHub</span></span>
* <span data-ttu-id="41d91-903">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="41d91-904">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-904">Az.KeyVault</span></span>
* <span data-ttu-id="41d91-905">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-906">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="41d91-906">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="41d91-907">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="41d91-907">Az.MachineLearning</span></span>
* <span data-ttu-id="41d91-908">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="41d91-909">Az.Media</span><span class="sxs-lookup"><span data-stu-id="41d91-909">Az.Media</span></span>
* <span data-ttu-id="41d91-910">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-911">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-911">Az.Monitor</span></span>
  * <span data-ttu-id="41d91-912">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-912">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="41d91-913">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="41d91-913">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="41d91-914">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="41d91-914">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="41d91-915">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="41d91-915">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="41d91-916">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="41d91-916">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="41d91-917">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="41d91-917">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="41d91-918">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="41d91-918">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-919">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-919">Az.Network</span></span>
* <span data-ttu-id="41d91-920">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-920">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-921">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="41d91-921">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="41d91-922">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="41d91-922">Az.NotificationHubs</span></span>
* <span data-ttu-id="41d91-923">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-924">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-924">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-925">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="41d91-926">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="41d91-926">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="41d91-927">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-928">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-928">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-929">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-930">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="41d91-930">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="41d91-931">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="41d91-931">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="41d91-932">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="41d91-932">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="41d91-933">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="41d91-933">Az.RedisCache</span></span>
* <span data-ttu-id="41d91-934">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-934">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-935">Az.Resources</span></span>
* <span data-ttu-id="41d91-936">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="41d91-936">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-937">Az.Sql</span></span>
* <span data-ttu-id="41d91-938">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="41d91-938">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="41d91-939">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-939">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-940">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="41d91-940">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="41d91-941">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="41d91-941">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="41d91-942">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="41d91-942">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="41d91-943">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-943">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="41d91-944">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="41d91-944">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-945">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-945">Az.Websites</span></span>
* <span data-ttu-id="41d91-946">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="41d91-946">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="41d91-947">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-947">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="41d91-948">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="41d91-948">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="41d91-949">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="41d91-949">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="41d91-950">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="41d91-950">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="41d91-951">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="41d91-951">Highlights since the last major release</span></span>
* <span data-ttu-id="41d91-952">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="41d91-952">General availability of `Az` module</span></span>
* <span data-ttu-id="41d91-953">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="41d91-953">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="41d91-954">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="41d91-954">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="41d91-955">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-955">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="41d91-956">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="41d91-956">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="41d91-957">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-957">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="41d91-958">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-958">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="41d91-959">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-959">Az.Accounts</span></span>
* <span data-ttu-id="41d91-960">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-960">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="41d91-961">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="41d91-961">Az.AnalysisServices</span></span>
* <span data-ttu-id="41d91-962">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="41d91-962">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="41d91-963">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="41d91-963">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-964">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-964">Az.Automation</span></span>
* <span data-ttu-id="41d91-965">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="41d91-965">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="41d91-966">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="41d91-966">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="41d91-967">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="41d91-967">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-968">Az.Compute</span></span>
* <span data-ttu-id="41d91-969">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-969">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="41d91-970">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="41d91-970">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="41d91-971">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-971">Az.ContainerInstance</span></span>
* <span data-ttu-id="41d91-972">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="41d91-972">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-973">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-973">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-974">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="41d91-974">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="41d91-975">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-975">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-976">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-976">Az.Resources</span></span>
* <span data-ttu-id="41d91-977">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="41d91-977">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="41d91-978">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="41d91-978">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="41d91-979">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="41d91-979">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="41d91-980">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="41d91-980">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="41d91-981">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="41d91-981">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="41d91-982">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="41d91-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-983">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-983">Az.Sql</span></span>
* <span data-ttu-id="41d91-984">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="41d91-984">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-985">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-985">Az.Storage</span></span>
* <span data-ttu-id="41d91-986">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="41d91-986">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="41d91-987">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="41d91-987">New-AzStorageContext</span></span>
* <span data-ttu-id="41d91-988">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="41d91-988">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="41d91-989">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="41d91-989">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="41d91-990">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="41d91-990">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="41d91-991">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-991">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="41d91-992">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-992">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="41d91-993">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-993">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="41d91-994">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41d91-994">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="41d91-995">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41d91-995">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="41d91-996">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41d91-996">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="41d91-997">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="41d91-997">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="41d91-998">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="41d91-998">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="41d91-999">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="41d91-999">Highlights since the last major release</span></span>
* <span data-ttu-id="41d91-1000">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="41d91-1000">General availability of `Az` module</span></span>
* <span data-ttu-id="41d91-1001">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="41d91-1001">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="41d91-1002">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="41d91-1002">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="41d91-1003">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1003">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="41d91-1004">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="41d91-1004">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="41d91-1005">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1005">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="41d91-1006">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1006">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-1007">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-1007">Az.Automation</span></span>
* <span data-ttu-id="41d91-1008">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="41d91-1008">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="41d91-1009">動態分組</span><span class="sxs-lookup"><span data-stu-id="41d91-1009">Dynamic grouping</span></span>
    * <span data-ttu-id="41d91-1010">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="41d91-1010">Pre-Post script</span></span>
    * <span data-ttu-id="41d91-1011">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="41d91-1011">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1012">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1012">Az.Compute</span></span>
* <span data-ttu-id="41d91-1013">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1013">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="41d91-1014">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="41d91-1014">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="41d91-1015">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-1015">Az.KeyVault</span></span>
* <span data-ttu-id="41d91-1016">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1016">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1017">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1017">Az.Network</span></span>
* <span data-ttu-id="41d91-1018">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1018">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="41d91-1019">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="41d91-1019">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1020">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1020">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-1021">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="41d91-1021">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="41d91-1022">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1022">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1023">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1023">Az.Resources</span></span>
* <span data-ttu-id="41d91-1024">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1024">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="41d91-1025">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="41d91-1025">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1026">Az.Sql</span></span>
* <span data-ttu-id="41d91-1027">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="41d91-1027">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-1028">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1028">Az.Storage</span></span>
* <span data-ttu-id="41d91-1029">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="41d91-1029">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="41d91-1030">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-1030">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="41d91-1031">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-1031">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="41d91-1032">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-1032">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="41d91-1033">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="41d91-1033">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="41d91-1034">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="41d91-1034">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="41d91-1035">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="41d91-1035">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-1036">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1036">Az.Websites</span></span>
* <span data-ttu-id="41d91-1037">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="41d91-1037">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="41d91-1038">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1038">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1039">Az.Accounts</span></span>
* <span data-ttu-id="41d91-1040">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1040">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="41d91-1041">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1041">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-1042">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-1042">Az.Automation</span></span>
* <span data-ttu-id="41d91-1043">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1043">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="41d91-1044">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1044">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="41d91-1045">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="41d91-1045">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="41d91-1046">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="41d91-1046">Az.Cdn</span></span>
* <span data-ttu-id="41d91-1047">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1047">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1048">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1048">Az.Compute</span></span>
* <span data-ttu-id="41d91-1049">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1049">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-1050">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-1050">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-1051">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="41d91-1051">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="41d91-1052">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="41d91-1052">Az.LogicApp</span></span>
* <span data-ttu-id="41d91-1053">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="41d91-1053">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1054">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1054">Az.Network</span></span>
* <span data-ttu-id="41d91-1055">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1055">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1056">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1056">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-1057">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1057">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="41d91-1058">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="41d91-1058">SDK Update</span></span>
* <span data-ttu-id="41d91-1059">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="41d91-1059">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="41d91-1060">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="41d91-1060">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1061">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1061">Az.Resources</span></span>
* <span data-ttu-id="41d91-1062">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1062">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="41d91-1063">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="41d91-1063">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="41d91-1064">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1064">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="41d91-1065">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="41d91-1065">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="41d91-1066">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1066">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="41d91-1067">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="41d91-1067">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1068">Az.Sql</span></span>
* <span data-ttu-id="41d91-1069">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="41d91-1069">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="41d91-1070">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="41d91-1070">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-1071">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1071">Az.Storage</span></span>
* <span data-ttu-id="41d91-1072">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="41d91-1072">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="41d91-1073">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1073">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="41d91-1074">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1074">Az.AnalysisServices</span></span>
* <span data-ttu-id="41d91-1075">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1075">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-1076">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-1076">Az.Automation</span></span>
* <span data-ttu-id="41d91-1077">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="41d91-1077">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="41d91-1078">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1078">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="41d91-1079">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="41d91-1079">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-1080">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1080">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-1081">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="41d91-1081">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1082">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1082">Az.Compute</span></span>
* <span data-ttu-id="41d91-1083">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1083">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="41d91-1084">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="41d91-1084">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="41d91-1085">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1085">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="41d91-1086">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="41d91-1086">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1087">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1087">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-1088">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1088">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="41d91-1089">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="41d91-1089">Az.EventHub</span></span>
* <span data-ttu-id="41d91-1090">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="41d91-1090">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="41d91-1091">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-1091">Az.KeyVault</span></span>
* <span data-ttu-id="41d91-1092">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="41d91-1092">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="41d91-1093">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="41d91-1093">Az.LogicApp</span></span>
* <span data-ttu-id="41d91-1094">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="41d91-1094">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="41d91-1095">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="41d91-1095">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="41d91-1096">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1096">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="41d91-1097">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="41d91-1097">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="41d91-1098">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="41d91-1098">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="41d91-1099">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="41d91-1099">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="41d91-1100">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="41d91-1100">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="41d91-1101">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1101">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="41d91-1102">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d91-1102">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="41d91-1103">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d91-1103">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="41d91-1104">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d91-1104">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="41d91-1105">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d91-1105">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="41d91-1106">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="41d91-1106">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="41d91-1107">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-1107">Az.Monitor</span></span>
* <span data-ttu-id="41d91-1108">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="41d91-1108">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1109">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1109">Az.Network</span></span>
* <span data-ttu-id="41d91-1110">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1110">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-1111">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-1111">Az.OperationalInsights</span></span>
* <span data-ttu-id="41d91-1112">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-1112">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="41d91-1113">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="41d91-1113">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="41d91-1114">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="41d91-1114">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="41d91-1115">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1115">Az.Resources</span></span>
* <span data-ttu-id="41d91-1116">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1116">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="41d91-1117">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="41d91-1118">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="41d91-1119">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="41d91-1119">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1120">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1120">Az.Sql</span></span>
* <span data-ttu-id="41d91-1121">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1121">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="41d91-1122">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="41d91-1122">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-1123">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1123">Az.Websites</span></span>
* <span data-ttu-id="41d91-1124">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1124">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="41d91-1125">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1125">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-1126">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1126">Az.Accounts</span></span>
* <span data-ttu-id="41d91-1127">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="41d91-1127">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="41d91-1128">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1128">Az.AnalysisServices</span></span>
<span data-ttu-id="41d91-1129">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="41d91-1129">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1130">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1130">Az.Compute</span></span>
* <span data-ttu-id="41d91-1131">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1131">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="41d91-1132">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="41d91-1132">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="41d91-1133">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1133">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1134">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1134">Az.RecoveryServices</span></span>
<span data-ttu-id="41d91-1135">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="41d91-1135">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1136">Az.Resources</span></span>
* <span data-ttu-id="41d91-1137">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="41d91-1137">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="41d91-1138">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="41d91-1138">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="41d91-1139">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1139">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="41d91-1140">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="41d91-1140">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1141">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1141">Az.Sql</span></span>
* <span data-ttu-id="41d91-1142">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="41d91-1142">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="41d91-1143">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1143">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="41d91-1144">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="41d91-1144">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="41d91-1145">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1145">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-1146">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1146">Az.Accounts</span></span>
* <span data-ttu-id="41d91-1147">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="41d91-1147">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="41d91-1148">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1148">Az.AnalysisServices</span></span>
* <span data-ttu-id="41d91-1149">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="41d91-1149">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1150">Az.RecoveryServices</span></span>
* <span data-ttu-id="41d91-1151">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="41d91-1151">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="41d91-1152">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1152">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-1153">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1153">Az.Accounts</span></span>
* <span data-ttu-id="41d91-1154">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="41d91-1154">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="41d91-1155">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1155">Update incorrect online help URLs</span></span>
* <span data-ttu-id="41d91-1156">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-1156">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="41d91-1157">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="41d91-1157">Az.Aks</span></span>
* <span data-ttu-id="41d91-1158">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1158">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="41d91-1159">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-1159">Az.Automation</span></span>
* <span data-ttu-id="41d91-1160">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1160">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="41d91-1161">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1161">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="41d91-1162">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="41d91-1162">Az.Cdn</span></span>
* <span data-ttu-id="41d91-1163">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1163">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1164">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1164">Az.Compute</span></span>
* <span data-ttu-id="41d91-1165">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1165">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="41d91-1166">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="41d91-1166">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="41d91-1167">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-1167">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="41d91-1168">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="41d91-1168">Az.ContainerRegistry</span></span>
* <span data-ttu-id="41d91-1169">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1169">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="41d91-1170">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="41d91-1170">Az.DataFactory</span></span>
* <span data-ttu-id="41d91-1171">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="41d91-1171">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1172">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1172">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-1173">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1173">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="41d91-1174">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="41d91-1174">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="41d91-1175">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1175">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-1176">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-1176">Az.IotHub</span></span>
* <span data-ttu-id="41d91-1177">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-1177">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="41d91-1178">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-1178">Az.KeyVault</span></span>
* <span data-ttu-id="41d91-1179">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1179">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1180">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1180">Az.Network</span></span>
* <span data-ttu-id="41d91-1181">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1181">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1182">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1182">Az.Resources</span></span>
* <span data-ttu-id="41d91-1183">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1183">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="41d91-1184">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1184">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="41d91-1185">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="41d91-1185">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="41d91-1186">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1186">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="41d91-1187">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1187">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="41d91-1188">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1188">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="41d91-1189">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="41d91-1189">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-1190">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-1190">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-1191">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="41d91-1191">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="41d91-1192">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="41d91-1192">Fix some error messages.</span></span>
* <span data-ttu-id="41d91-1193">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1193">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="41d91-1194">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1194">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="41d91-1195">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="41d91-1195">Az.SignalR</span></span>
* <span data-ttu-id="41d91-1196">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1196">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1197">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1197">Az.Sql</span></span>
* <span data-ttu-id="41d91-1198">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1198">Update incorrect online help URLs</span></span>
* <span data-ttu-id="41d91-1199">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="41d91-1199">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="41d91-1200">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1200">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="41d91-1201">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="41d91-1201">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-1202">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1202">Az.Storage</span></span>
* <span data-ttu-id="41d91-1203">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1203">Update incorrect online help URLs</span></span>
* <span data-ttu-id="41d91-1204">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="41d91-1204">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="41d91-1205">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="41d91-1205">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="41d91-1206">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="41d91-1206">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="41d91-1207">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="41d91-1207">Az.TrafficManager</span></span>
* <span data-ttu-id="41d91-1208">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1208">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-1209">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1209">Az.Websites</span></span>
* <span data-ttu-id="41d91-1210">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1210">Update incorrect online help URLs</span></span>
* <span data-ttu-id="41d91-1211">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="41d91-1211">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="41d91-1212">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="41d91-1212">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="41d91-1213">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1213">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="41d91-1214">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1214">Az.Accounts</span></span>
* <span data-ttu-id="41d91-1215">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="41d91-1215">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1216">Az.Compute</span></span>
* <span data-ttu-id="41d91-1217">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="41d91-1217">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="41d91-1218">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="41d91-1218">Updated the description of ID in help files</span></span>
* <span data-ttu-id="41d91-1219">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1219">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1220">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1220">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-1221">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1221">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="41d91-1222">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="41d91-1222">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="41d91-1223">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="41d91-1223">Az.EventGrid</span></span>
* <span data-ttu-id="41d91-1224">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="41d91-1224">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="41d91-1225">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="41d91-1225">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="41d91-1226">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="41d91-1226">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="41d91-1227">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="41d91-1227">Event Time-To-Live,</span></span>
        - <span data-ttu-id="41d91-1228">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="41d91-1228">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="41d91-1229">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="41d91-1229">Dead letter endpoint.</span></span>
    - <span data-ttu-id="41d91-1230">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="41d91-1230">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="41d91-1231">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="41d91-1231">Event Time-To-Live,</span></span>
        - <span data-ttu-id="41d91-1232">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="41d91-1232">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="41d91-1233">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="41d91-1233">Dead letter endpoint.</span></span>
* <span data-ttu-id="41d91-1234">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="41d91-1234">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="41d91-1235">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="41d91-1235">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="41d91-1236">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="41d91-1236">Az.IotHub</span></span>
* <span data-ttu-id="41d91-1237">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="41d91-1237">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="41d91-1238">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="41d91-1238">Az.LogicApp</span></span>
* <span data-ttu-id="41d91-1239">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-1239">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1240">Az.Resources</span></span>
* <span data-ttu-id="41d91-1241">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1241">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="41d91-1242">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="41d91-1242">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="41d91-1243">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="41d91-1243">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="41d91-1244">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-1244">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="41d91-1245">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="41d91-1245">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="41d91-1246">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="41d91-1246">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="41d91-1247">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="41d91-1247">Az.SignalR</span></span>
* <span data-ttu-id="41d91-1248">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1248">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1249">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1249">Az.Sql</span></span>
* <span data-ttu-id="41d91-1250">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="41d91-1250">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="41d91-1251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1251">Az.Storage</span></span>
* <span data-ttu-id="41d91-1252">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-1252">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="41d91-1253">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="41d91-1253">New-AzStorageContext</span></span>
* <span data-ttu-id="41d91-1254">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="41d91-1254">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="41d91-1255">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="41d91-1255">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-1256">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1256">Az.Websites</span></span>
* <span data-ttu-id="41d91-1257">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="41d91-1257">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="41d91-1258">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1258">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="41d91-1259">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1259">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="41d91-1260">一般</span><span class="sxs-lookup"><span data-stu-id="41d91-1260">General</span></span>

- <span data-ttu-id="41d91-1261">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="41d91-1261">General Availability of Az Module</span></span>
- <span data-ttu-id="41d91-1262">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="41d91-1262">Online help for each module</span></span>
- <span data-ttu-id="41d91-1263">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="41d91-1263">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="41d91-1264">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1264">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="41d91-1265">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1265">Az.Accounts</span></span>
- <span data-ttu-id="41d91-1266">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="41d91-1266">Changed from Az.Profile</span></span>
- <span data-ttu-id="41d91-1267">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="41d91-1267">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="41d91-1268">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-1268">Az.ApiManagement</span></span>
- <span data-ttu-id="41d91-1269">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="41d91-1269">Fixes for #7002</span></span>
- <span data-ttu-id="41d91-1270">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1270">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="41d91-1271">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="41d91-1271">Az.Batch</span></span>
- <span data-ttu-id="41d91-1272">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="41d91-1272">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="41d91-1273">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="41d91-1273">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="41d91-1274">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1274">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="41d91-1275">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="41d91-1275">Az.Billing</span></span>
- <span data-ttu-id="41d91-1276">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1276">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="41d91-1277">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1277">Az.CognitivServices</span></span>
- <span data-ttu-id="41d91-1278">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="41d91-1278">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="41d91-1279">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="41d91-1279">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="41d91-1280">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1280">Az.ContainerInstance</span></span>
- <span data-ttu-id="41d91-1281">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1281">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="41d91-1282">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="41d91-1282">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="41d91-1283">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1283">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1284">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1284">Az.DataLakeStore</span></span>
- <span data-ttu-id="41d91-1285">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="41d91-1286">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="41d91-1286">Az.Monitor</span></span>
- <span data-ttu-id="41d91-1287">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1287">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="41d91-1288">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="41d91-1288">Az.KeyVault</span></span>
- <span data-ttu-id="41d91-1289">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="41d91-1289">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="41d91-1290">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="41d91-1290">Az.MachineLearning</span></span>
- <span data-ttu-id="41d91-1291">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1291">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="41d91-1292">Az.Media</span><span class="sxs-lookup"><span data-stu-id="41d91-1292">Az.Media</span></span>
- <span data-ttu-id="41d91-1293">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="41d91-1293">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="41d91-1294">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1294">Az.Network</span></span>
<span data-ttu-id="41d91-1295">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1295">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="41d91-1296">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="41d91-1296">New cmdlets added:</span></span>
        - <span data-ttu-id="41d91-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1297">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1298">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1299">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1300">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1301">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1302">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="41d91-1302">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="41d91-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1303">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="41d91-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="41d91-1304">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="41d91-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d91-1305">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="41d91-1306">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41d91-1306">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="41d91-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="41d91-1307">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="41d91-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="41d91-1308">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="41d91-1309">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-1309">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="41d91-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-1310">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="41d91-1311">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-1311">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="41d91-1312">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1312">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="41d91-1313">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="41d91-1313">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="41d91-1314">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="41d91-1314">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="41d91-1315">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="41d91-1315">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="41d91-1316">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1316">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="41d91-1317">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1317">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="41d91-1318">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-1318">Az.OperationalInsights</span></span>
- <span data-ttu-id="41d91-1319">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="41d91-1320">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="41d91-1320">Az.Profile</span></span>
- <span data-ttu-id="41d91-1321">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="41d91-1321">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1322">Az.RecoveryServices</span></span>
- <span data-ttu-id="41d91-1323">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1323">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="41d91-1324">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1324">Az.Resources</span></span>
- <span data-ttu-id="41d91-1325">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="41d91-1326">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-1326">Az.ServiceFabric</span></span>
- <span data-ttu-id="41d91-1327">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="41d91-1327">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="41d91-1328">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1328">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="41d91-1329">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="41d91-1329">Az.SIgnalR</span></span>
- <span data-ttu-id="41d91-1330">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="41d91-1330">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="41d91-1331">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1331">Az.Sql</span></span>
- <span data-ttu-id="41d91-1332">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="41d91-1332">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="41d91-1333">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1333">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="41d91-1334">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1334">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="41d91-1335">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1335">Az.Storage</span></span>
- <span data-ttu-id="41d91-1336">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="41d91-1337">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1337">Az.Websites</span></span>
- <span data-ttu-id="41d91-1338">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="41d91-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="41d91-1339">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1339">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="41d91-1340">一般</span><span class="sxs-lookup"><span data-stu-id="41d91-1340">General</span></span>

* <span data-ttu-id="41d91-1341">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="41d91-1341">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="41d91-1342">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1342">Az.Compute</span></span>

* <span data-ttu-id="41d91-1343">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="41d91-1343">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1344">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1344">Az.DataLakeStore</span></span>

* <span data-ttu-id="41d91-1345">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="41d91-1345">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="41d91-1346">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="41d91-1346">Az.FrontDoor</span></span>

* <span data-ttu-id="41d91-1347">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="41d91-1347">Fixed some broken links</span></span>
    - <span data-ttu-id="41d91-1348">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="41d91-1348">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="41d91-1349">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="41d91-1349">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="41d91-1350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1350">Az.RecoveryServices</span></span>

* <span data-ttu-id="41d91-1351">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="41d91-1351">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="41d91-1352">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="41d91-1352">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="41d91-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1353">Az.Resources</span></span>

* <span data-ttu-id="41d91-1354">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="41d91-1354">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="41d91-1355">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="41d91-1355">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="41d91-1356">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1356">Az.Sql</span></span>

* <span data-ttu-id="41d91-1357">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="41d91-1357">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="41d91-1358">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1358">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="41d91-1359">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="41d91-1359">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="41d91-1360">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1360">Az.Storage</span></span>

* <span data-ttu-id="41d91-1361">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="41d91-1361">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="41d91-1362">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="41d91-1362">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="41d91-1363">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="41d91-1363">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="41d91-1364">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="41d91-1364">Support Static Website configuration</span></span>
    - <span data-ttu-id="41d91-1365">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="41d91-1365">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="41d91-1366">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="41d91-1366">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="41d91-1367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1367">Az.Websites</span></span>

* <span data-ttu-id="41d91-1368">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41d91-1368">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="41d91-1369">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="41d91-1369">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="41d91-1370">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="41d91-1370">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="41d91-1371">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1371">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="41d91-1372">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="41d91-1372">Az.ApiManagement</span></span>
* <span data-ttu-id="41d91-1373">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="41d91-1373">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="41d91-1374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="41d91-1374">Az.Automation</span></span>
* <span data-ttu-id="41d91-1375">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1375">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="41d91-1376">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1376">Added Update Management cmdlets</span></span>
* <span data-ttu-id="41d91-1377">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1377">Added Source Control cmdlets</span></span>
* <span data-ttu-id="41d91-1378">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1378">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="41d91-1379">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="41d91-1379">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="41d91-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1380">Az.Compute</span></span>
* <span data-ttu-id="41d91-1381">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1381">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="41d91-1382">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="41d91-1382">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="41d91-1383">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1383">Az.ContainerInstance</span></span>
* <span data-ttu-id="41d91-1384">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="41d91-1384">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="41d91-1385">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="41d91-1385">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="41d91-1386">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="41d91-1386">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="41d91-1387">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1387">Az.Network</span></span>
* <span data-ttu-id="41d91-1388">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="41d91-1388">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="41d91-1389">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="41d91-1389">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="41d91-1390">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="41d91-1390">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="41d91-1391">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1391">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="41d91-1392">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="41d91-1392">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="41d91-1393">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="41d91-1393">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="41d91-1394">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="41d91-1394">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="41d91-1395">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="41d91-1395">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="41d91-1396">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1396">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="41d91-1397">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="41d91-1397">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="41d91-1398">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="41d91-1398">Az.Relay</span></span>
* <span data-ttu-id="41d91-1399">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="41d91-1399">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="41d91-1400">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1400">Az.Resources</span></span>
* <span data-ttu-id="41d91-1401">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="41d91-1401">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="41d91-1402">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="41d91-1402">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="41d91-1403">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="41d91-1403">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="41d91-1404">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-1404">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-1405">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="41d91-1405">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="41d91-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1406">Az.Sql</span></span>
* <span data-ttu-id="41d91-1407">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1407">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="41d91-1408">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1408">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="41d91-1409">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1409">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="41d91-1410">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1410">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="41d91-1411">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="41d91-1411">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="41d91-1412">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="41d91-1412">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="41d91-1413">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="41d91-1413">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="41d91-1414">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="41d91-1414">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="41d91-1415">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="41d91-1415">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="41d91-1416">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="41d91-1416">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="41d91-1417">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="41d91-1417">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="41d91-1418">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="41d91-1418">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="41d91-1419">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="41d91-1419">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="41d91-1420">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="41d91-1420">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="41d91-1421">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="41d91-1421">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="41d91-1422">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="41d91-1422">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="41d91-1423">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1423">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="41d91-1424">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1424">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="41d91-1425">一般</span><span class="sxs-lookup"><span data-stu-id="41d91-1425">General</span></span>
* <span data-ttu-id="41d91-1426">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="41d91-1426">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="41d91-1427">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="41d91-1427">Az.Profile</span></span>
* <span data-ttu-id="41d91-1428">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="41d91-1428">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="41d91-1429">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="41d91-1429">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="41d91-1430">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="41d91-1430">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="41d91-1431">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="41d91-1431">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="41d91-1432">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1432">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="41d91-1433">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1433">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="41d91-1434">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1434">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-1435">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1435">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-1436">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="41d91-1436">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1437">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1437">Az.Compute</span></span>
* <span data-ttu-id="41d91-1438">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1438">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="41d91-1439">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="41d91-1439">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="41d91-1440">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1440">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-1442">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="41d91-1442">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="41d91-1443">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="41d91-1443">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="41d91-1444">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="41d91-1444">Az.Insights</span></span>
* <span data-ttu-id="41d91-1445">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="41d91-1445">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="41d91-1446">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1446">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="41d91-1447">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="41d91-1447">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="41d91-1448">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="41d91-1448">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1449">Az.Network</span></span>
* <span data-ttu-id="41d91-1450">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="41d91-1450">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="41d91-1451">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="41d91-1451">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="41d91-1452">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="41d91-1452">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="41d91-1453">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="41d91-1453">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="41d91-1454">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="41d91-1454">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="41d91-1455">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="41d91-1455">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="41d91-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="41d91-1456">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="41d91-1457">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="41d91-1457">Az.PolicyInsights</span></span>
* <span data-ttu-id="41d91-1458">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1458">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1459">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1459">Az.Resources</span></span>
* <span data-ttu-id="41d91-1460">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="41d91-1460">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="41d91-1461">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="41d91-1461">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="41d91-1462">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="41d91-1462">Az.ServiceBus</span></span>
* <span data-ttu-id="41d91-1463">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="41d91-1463">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="41d91-1464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="41d91-1464">Az.ServiceFabric</span></span>
* <span data-ttu-id="41d91-1465">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="41d91-1465">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="41d91-1466">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="41d91-1466">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="41d91-1467">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="41d91-1467">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="41d91-1468">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="41d91-1468">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="41d91-1469">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="41d91-1469">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="41d91-1470">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1470">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="41d91-1471">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="41d91-1471">Az.Profile</span></span>
* <span data-ttu-id="41d91-1472">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1472">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="41d91-1473">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="41d91-1473">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1474">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1474">Az.Compute</span></span>
* <span data-ttu-id="41d91-1475">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="41d91-1475">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="41d91-1476">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-1476">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="41d91-1477">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="41d91-1477">Az.DataLakeStore</span></span>
* <span data-ttu-id="41d91-1478">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="41d91-1478">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="41d91-1479">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="41d91-1479">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="41d91-1480">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="41d91-1480">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="41d91-1481">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="41d91-1481">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="41d91-1482">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="41d91-1482">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1483">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1483">Az.Network</span></span>
* <span data-ttu-id="41d91-1484">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="41d91-1484">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="41d91-1485">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41d91-1485">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1486">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1486">Az.Resources</span></span>
* <span data-ttu-id="41d91-1487">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="41d91-1487">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="41d91-1488">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="41d91-1488">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="41d91-1489">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1489">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="41d91-1490">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="41d91-1490">Azure.Storage</span></span>
* <span data-ttu-id="41d91-1491">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1491">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="41d91-1492">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="41d91-1492">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="41d91-1493">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="41d91-1493">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="41d91-1494">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="41d91-1494">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="41d91-1495">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="41d91-1495">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="41d91-1496">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="41d91-1496">Az.CognitiveServices</span></span>
* <span data-ttu-id="41d91-1497">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="41d91-1497">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="41d91-1498">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="41d91-1498">Az.Compute</span></span>
* <span data-ttu-id="41d91-1499">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="41d91-1499">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="41d91-1500">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="41d91-1500">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="41d91-1501">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="41d91-1501">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="41d91-1502">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="41d91-1502">Az.DataFactoryV2</span></span>
* <span data-ttu-id="41d91-1503">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="41d91-1503">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="41d91-1504">Az.Network</span><span class="sxs-lookup"><span data-stu-id="41d91-1504">Az.Network</span></span>
* <span data-ttu-id="41d91-1505">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="41d91-1505">Added NetworkProfile functionality.</span></span> <span data-ttu-id="41d91-1506">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1506">new cmdlets added</span></span>
    - <span data-ttu-id="41d91-1507">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="41d91-1507">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="41d91-1508">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="41d91-1508">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="41d91-1509">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="41d91-1509">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="41d91-1510">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="41d91-1510">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="41d91-1511">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-1511">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="41d91-1512">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="41d91-1512">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="41d91-1513">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="41d91-1513">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="41d91-1514">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1514">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="41d91-1515">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d91-1515">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="41d91-1516">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="41d91-1516">Az.RedisCache</span></span>
* <span data-ttu-id="41d91-1517">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="41d91-1517">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="41d91-1518">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="41d91-1518">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="41d91-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="41d91-1519">Az.Resources</span></span>
* <span data-ttu-id="41d91-1520">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="41d91-1520">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="41d91-1521">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="41d91-1521">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="41d91-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="41d91-1522">Az.Sql</span></span>
* <span data-ttu-id="41d91-1523">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="41d91-1523">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="41d91-1524">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="41d91-1524">Az.Websites</span></span>
* <span data-ttu-id="41d91-1525">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="41d91-1525">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="41d91-1526">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="41d91-1526">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="41d91-1527">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="41d91-1527">0.2.0 - September 2018</span></span>
 <span data-ttu-id="41d91-1528">初始版本</span><span class="sxs-lookup"><span data-stu-id="41d91-1528">Initial Release</span></span>
