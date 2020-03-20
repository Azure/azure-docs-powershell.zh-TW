---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111038"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="05f43-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="05f43-104">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="05f43-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-105">Az.Accounts</span></span>
* <span data-ttu-id="05f43-106">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="05f43-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="05f43-107">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="05f43-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="05f43-108">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="05f43-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="05f43-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-109">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-110">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="05f43-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="05f43-111">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="05f43-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="05f43-112">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="05f43-113">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="05f43-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-115">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="05f43-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-116">Az.IotHub</span></span>
* <span data-ttu-id="05f43-117">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="05f43-118">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="05f43-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="05f43-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="05f43-123">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="05f43-124">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="05f43-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="05f43-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="05f43-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="05f43-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="05f43-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="05f43-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="05f43-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="05f43-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="05f43-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="05f43-129">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="05f43-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="05f43-130">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="05f43-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="05f43-131">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="05f43-132">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="05f43-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="05f43-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="05f43-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="05f43-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="05f43-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="05f43-135">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-136">Az.Monitor</span></span>
* <span data-ttu-id="05f43-137">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="05f43-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-138">Az.Network</span></span>
* <span data-ttu-id="05f43-139">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="05f43-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="05f43-140">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="05f43-141">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="05f43-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="05f43-142">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="05f43-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-143">Az.Resources</span></span>
* <span data-ttu-id="05f43-144">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="05f43-145">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="05f43-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="05f43-146">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="05f43-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="05f43-147">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="05f43-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="05f43-148">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="05f43-149">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="05f43-150">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="05f43-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="05f43-151">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f43-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="05f43-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f43-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="05f43-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f43-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="05f43-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f43-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="05f43-155">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="05f43-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="05f43-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="05f43-157">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="05f43-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-158">Az.Sql</span></span>
* <span data-ttu-id="05f43-159">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="05f43-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="05f43-160">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="05f43-161">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="05f43-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="05f43-162">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="05f43-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="05f43-163">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="05f43-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="05f43-164">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="05f43-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="05f43-165">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="05f43-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="05f43-166">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="05f43-167">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="05f43-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-168">Az.Storage</span></span>
* <span data-ttu-id="05f43-169">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="05f43-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="05f43-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="05f43-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="05f43-171">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="05f43-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="05f43-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="05f43-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="05f43-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-174">Az.Websites</span></span>
* <span data-ttu-id="05f43-175">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="05f43-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="05f43-176">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="05f43-177">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="05f43-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="05f43-178">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="05f43-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="05f43-179">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="05f43-180">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="05f43-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-181">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-181">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-182">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="05f43-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="05f43-183">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="05f43-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="05f43-184">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-185">Az.Accounts</span></span>
* <span data-ttu-id="05f43-186">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="05f43-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-187">Az.Automation</span></span>
* <span data-ttu-id="05f43-188">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-190">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="05f43-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="05f43-191">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-192">Az.Compute</span></span>
* <span data-ttu-id="05f43-193">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="05f43-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-194">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-195">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="05f43-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-196">Az.IotHub</span></span>
* <span data-ttu-id="05f43-197">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="05f43-198">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="05f43-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="05f43-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="05f43-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="05f43-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-203">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-204">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="05f43-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-205">Az.Monitor</span></span>
* <span data-ttu-id="05f43-206">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="05f43-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="05f43-207">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="05f43-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="05f43-208">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="05f43-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-209">Az.Network</span></span>
* <span data-ttu-id="05f43-210">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="05f43-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="05f43-211">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="05f43-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="05f43-212">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="05f43-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="05f43-213">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="05f43-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="05f43-214">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-214">No new cmdlets are added.</span></span> <span data-ttu-id="05f43-215">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="05f43-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-217">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-218">Az.Resources</span></span>
* <span data-ttu-id="05f43-219">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="05f43-220">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="05f43-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="05f43-221">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="05f43-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="05f43-222">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="05f43-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="05f43-223">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="05f43-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="05f43-224">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="05f43-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="05f43-225">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="05f43-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="05f43-226">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="05f43-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-227">Az.Sql</span></span>
* <span data-ttu-id="05f43-228">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="05f43-229">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="05f43-230">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="05f43-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="05f43-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="05f43-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="05f43-232">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="05f43-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="05f43-233">Az.StorageSync</span></span>
* <span data-ttu-id="05f43-234">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="05f43-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="05f43-235">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="05f43-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-236">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-236">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-237">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="05f43-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="05f43-238">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="05f43-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-239">Az.Accounts</span></span>
* <span data-ttu-id="05f43-240">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="05f43-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="05f43-241">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="05f43-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="05f43-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-242">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-243">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="05f43-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="05f43-244">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="05f43-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="05f43-245">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="05f43-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="05f43-246">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="05f43-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-247">Az.Compute</span></span>
* <span data-ttu-id="05f43-248">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="05f43-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="05f43-249">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="05f43-250">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="05f43-251">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="05f43-252">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-253">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-254">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="05f43-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="05f43-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="05f43-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="05f43-256">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="05f43-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="05f43-257">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="05f43-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="05f43-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-258">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-259">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="05f43-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-260">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-261">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="05f43-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-262">Az.Network</span></span>
* <span data-ttu-id="05f43-263">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="05f43-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="05f43-264">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="05f43-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="05f43-265">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="05f43-266">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="05f43-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="05f43-267">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="05f43-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="05f43-268">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="05f43-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="05f43-269">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="05f43-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="05f43-270">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="05f43-271">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-271">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="05f43-273">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="05f43-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="05f43-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="05f43-275">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="05f43-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="05f43-277">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="05f43-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="05f43-278">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="05f43-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="05f43-279">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="05f43-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="05f43-280">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="05f43-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-282">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="05f43-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="05f43-283">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-284">Az.Resources</span></span>
* <span data-ttu-id="05f43-285">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="05f43-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="05f43-286">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-287">Az.Sql</span></span>
<span data-ttu-id="05f43-288">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="05f43-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-289">Az.Storage</span></span>
* <span data-ttu-id="05f43-290">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="05f43-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="05f43-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="05f43-292">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="05f43-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="05f43-293">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="05f43-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-294">Az.Websites</span></span>
* <span data-ttu-id="05f43-295">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="05f43-296">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="05f43-297">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="05f43-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-298">Az.Accounts</span></span>
* <span data-ttu-id="05f43-299">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-300">Az.Cdn</span></span>
* <span data-ttu-id="05f43-301">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="05f43-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-302">Az.Compute</span></span>
* <span data-ttu-id="05f43-303">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="05f43-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="05f43-305">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="05f43-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="05f43-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="05f43-307">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="05f43-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="05f43-308">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="05f43-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="05f43-309">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="05f43-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="05f43-310">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="05f43-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="05f43-311">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="05f43-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="05f43-312">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="05f43-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="05f43-313">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="05f43-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="05f43-314">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="05f43-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="05f43-315">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="05f43-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="05f43-316">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="05f43-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="05f43-317">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="05f43-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="05f43-318">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="05f43-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="05f43-319">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="05f43-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="05f43-320">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="05f43-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="05f43-321">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="05f43-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="05f43-322">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="05f43-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="05f43-323">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="05f43-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="05f43-324">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="05f43-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-325">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-326">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="05f43-327">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="05f43-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="05f43-328">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="05f43-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="05f43-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="05f43-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="05f43-330">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="05f43-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-331">Az.EventHub</span></span>
* <span data-ttu-id="05f43-332">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="05f43-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="05f43-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-333">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-334">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="05f43-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="05f43-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="05f43-335">Az.MachineLearning</span></span>
* <span data-ttu-id="05f43-336">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="05f43-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="05f43-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="05f43-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="05f43-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="05f43-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="05f43-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="05f43-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="05f43-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="05f43-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="05f43-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="05f43-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="05f43-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="05f43-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="05f43-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-344">Az.Network</span></span>
* <span data-ttu-id="05f43-345">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="05f43-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-347">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="05f43-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="05f43-348">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="05f43-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="05f43-349">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="05f43-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="05f43-350">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="05f43-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-351">Az.Resources</span></span>
* <span data-ttu-id="05f43-352">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="05f43-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-353">Az.Sql</span></span>
* <span data-ttu-id="05f43-354">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="05f43-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="05f43-355">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="05f43-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="05f43-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="05f43-357">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="05f43-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-358">Az.Storage</span></span>
* <span data-ttu-id="05f43-359">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="05f43-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="05f43-361">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="05f43-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="05f43-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="05f43-363">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="05f43-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="05f43-364">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-364">General</span></span>
* <span data-ttu-id="05f43-365">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="05f43-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-366">Az.Accounts</span></span>
* <span data-ttu-id="05f43-367">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="05f43-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="05f43-368">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="05f43-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-369">Az.Batch</span></span>
* <span data-ttu-id="05f43-370">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f43-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-371">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-372">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="05f43-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-373">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-374">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="05f43-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="05f43-375">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="05f43-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="05f43-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="05f43-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="05f43-377">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="05f43-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-378">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-379">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="05f43-380">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="05f43-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="05f43-381">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-382">Az.Monitor</span></span>
* <span data-ttu-id="05f43-383">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="05f43-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="05f43-384">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="05f43-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="05f43-385">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="05f43-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-386">Az.Network</span></span>
* <span data-ttu-id="05f43-387">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="05f43-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-388">Az.Resources</span></span>
* <span data-ttu-id="05f43-389">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="05f43-390">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-391">Az.Sql</span></span>
* <span data-ttu-id="05f43-392">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="05f43-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-393">Az.Storage</span></span>
* <span data-ttu-id="05f43-394">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="05f43-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="05f43-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="05f43-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="05f43-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="05f43-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="05f43-397">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="05f43-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="05f43-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="05f43-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="05f43-399">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="05f43-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="05f43-400">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="05f43-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="05f43-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="05f43-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="05f43-403">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="05f43-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="05f43-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="05f43-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="05f43-405">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="05f43-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="05f43-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="05f43-407">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="05f43-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-408">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-408">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-409">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="05f43-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="05f43-410">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="05f43-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-411">Az.Compute</span></span>
* <span data-ttu-id="05f43-412">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="05f43-412">VM Reapply feature</span></span>
    - <span data-ttu-id="05f43-413">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="05f43-414">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="05f43-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="05f43-415">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="05f43-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="05f43-416">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="05f43-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="05f43-417">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="05f43-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="05f43-418">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="05f43-419">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="05f43-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="05f43-420">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="05f43-421">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="05f43-422">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="05f43-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="05f43-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="05f43-424">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="05f43-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="05f43-425">取得訂單</span><span class="sxs-lookup"><span data-stu-id="05f43-425">Get the Order</span></span>
* <span data-ttu-id="05f43-426">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="05f43-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="05f43-427">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="05f43-427">Create new Order</span></span>
* <span data-ttu-id="05f43-428">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="05f43-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="05f43-429">移除訂單</span><span class="sxs-lookup"><span data-stu-id="05f43-429">Remove the Order</span></span>
* <span data-ttu-id="05f43-430">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="05f43-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="05f43-431">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="05f43-431">Now creates Local Share</span></span>
* <span data-ttu-id="05f43-432">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="05f43-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="05f43-433">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="05f43-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="05f43-434">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="05f43-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="05f43-435">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="05f43-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="05f43-436">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="05f43-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="05f43-437">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="05f43-438">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="05f43-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="05f43-439">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="05f43-439">Create new Triggers</span></span>
* <span data-ttu-id="05f43-440">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="05f43-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="05f43-441">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="05f43-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-442">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-443">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="05f43-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="05f43-444">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="05f43-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-446">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="05f43-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-447">Az.EventHub</span></span>
* <span data-ttu-id="05f43-448">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="05f43-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-449">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-450">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="05f43-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="05f43-451">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="05f43-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="05f43-452">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="05f43-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="05f43-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="05f43-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-454">Az.Network</span></span>
* <span data-ttu-id="05f43-455">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="05f43-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="05f43-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="05f43-456">Az.PrivateDns</span></span>
* <span data-ttu-id="05f43-457">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="05f43-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-459">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="05f43-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="05f43-460">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="05f43-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="05f43-461">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="05f43-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="05f43-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="05f43-462">Az.RedisCache</span></span>
* <span data-ttu-id="05f43-463">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="05f43-464">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="05f43-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="05f43-465">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="05f43-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-466">Az.Resources</span></span>
- <span data-ttu-id="05f43-467">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="05f43-468">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="05f43-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="05f43-469">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="05f43-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="05f43-470">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="05f43-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="05f43-471">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="05f43-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-472">Az.Sql</span></span>
* <span data-ttu-id="05f43-473">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="05f43-474">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="05f43-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="05f43-475">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="05f43-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="05f43-476">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-476">General</span></span>
* <span data-ttu-id="05f43-477">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="05f43-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-478">Az.Accounts</span></span>
* <span data-ttu-id="05f43-479">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="05f43-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="05f43-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="05f43-480">Az.Advisor</span></span>
* <span data-ttu-id="05f43-481">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="05f43-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="05f43-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-482">Az.Batch</span></span>
* <span data-ttu-id="05f43-483">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="05f43-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="05f43-484">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="05f43-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="05f43-485">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="05f43-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="05f43-486">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="05f43-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="05f43-487">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="05f43-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="05f43-488">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="05f43-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="05f43-489">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="05f43-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="05f43-490">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="05f43-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="05f43-491">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="05f43-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="05f43-492">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="05f43-493">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="05f43-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="05f43-494">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="05f43-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="05f43-495">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="05f43-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="05f43-496">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="05f43-497">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="05f43-498">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="05f43-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="05f43-499">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="05f43-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="05f43-500">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="05f43-501">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="05f43-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="05f43-502">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="05f43-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="05f43-503">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="05f43-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="05f43-504">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="05f43-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="05f43-505">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="05f43-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="05f43-506">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="05f43-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="05f43-507">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="05f43-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="05f43-508">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="05f43-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="05f43-509">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="05f43-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="05f43-510">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="05f43-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="05f43-511">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="05f43-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="05f43-512">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="05f43-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="05f43-513">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="05f43-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="05f43-514">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="05f43-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="05f43-515">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="05f43-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="05f43-516">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="05f43-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="05f43-517">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="05f43-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="05f43-518">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="05f43-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-519">Az.Cdn</span></span>
* <span data-ttu-id="05f43-520">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="05f43-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="05f43-521">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="05f43-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-522">Az.Compute</span></span>
* <span data-ttu-id="05f43-523">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="05f43-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="05f43-524">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="05f43-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="05f43-525">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="05f43-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="05f43-526">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="05f43-527">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="05f43-528">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="05f43-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="05f43-529">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="05f43-530">重大變更</span><span class="sxs-lookup"><span data-stu-id="05f43-530">Breaking changes</span></span>
    - <span data-ttu-id="05f43-531">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="05f43-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="05f43-532">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="05f43-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-533">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-534">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="05f43-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-536">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="05f43-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="05f43-537">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05f43-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="05f43-538">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="05f43-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="05f43-539">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="05f43-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="05f43-540">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="05f43-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="05f43-541">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-542">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-543">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="05f43-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="05f43-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-544">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-545">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="05f43-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="05f43-546">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="05f43-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="05f43-547">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="05f43-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="05f43-548">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="05f43-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="05f43-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="05f43-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="05f43-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="05f43-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="05f43-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="05f43-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="05f43-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="05f43-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="05f43-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="05f43-554">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="05f43-555">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="05f43-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="05f43-556">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="05f43-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="05f43-557">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="05f43-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="05f43-558">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="05f43-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="05f43-559">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="05f43-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="05f43-560">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="05f43-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="05f43-561">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="05f43-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="05f43-562">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="05f43-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="05f43-563">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="05f43-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="05f43-564">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="05f43-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="05f43-565">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="05f43-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="05f43-566">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="05f43-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-567">Az.IotHub</span></span>
* <span data-ttu-id="05f43-568">重大變更：</span><span class="sxs-lookup"><span data-stu-id="05f43-568">Breaking changes:</span></span>
    - <span data-ttu-id="05f43-569">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="05f43-570">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="05f43-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="05f43-571">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="05f43-572">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="05f43-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="05f43-573">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="05f43-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="05f43-574">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="05f43-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="05f43-575">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="05f43-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="05f43-576">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="05f43-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="05f43-577">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="05f43-578">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="05f43-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="05f43-579">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="05f43-580">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="05f43-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-582">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="05f43-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-583">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="05f43-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="05f43-584">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="05f43-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="05f43-585">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="05f43-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-586">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="05f43-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-587">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="05f43-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-588">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="05f43-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-589">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-590">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="05f43-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-591">Az.Resources</span></span>
* <span data-ttu-id="05f43-592">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="05f43-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-593">Az.Network</span></span>
* <span data-ttu-id="05f43-594">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="05f43-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="05f43-595">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="05f43-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="05f43-601">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="05f43-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="05f43-602">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-602">New cmdlet:</span></span>
        - <span data-ttu-id="05f43-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="05f43-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="05f43-604">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="05f43-605">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="05f43-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="05f43-606">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="05f43-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="05f43-607">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="05f43-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="05f43-608">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="05f43-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="05f43-609">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="05f43-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="05f43-610">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="05f43-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="05f43-611">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-611">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="05f43-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="05f43-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="05f43-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="05f43-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="05f43-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="05f43-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="05f43-617">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="05f43-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="05f43-618">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="05f43-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="05f43-619">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="05f43-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="05f43-620">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="05f43-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="05f43-621">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="05f43-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="05f43-622">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="05f43-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="05f43-623">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="05f43-624">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-624">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="05f43-626">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="05f43-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="05f43-627">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="05f43-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="05f43-628">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="05f43-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="05f43-629">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="05f43-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="05f43-630">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="05f43-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="05f43-631">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="05f43-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="05f43-632">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="05f43-633">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-633">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="05f43-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="05f43-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="05f43-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="05f43-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="05f43-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="05f43-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="05f43-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="05f43-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="05f43-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="05f43-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="05f43-640">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="05f43-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="05f43-641">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="05f43-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="05f43-642">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="05f43-643">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="05f43-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="05f43-644">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="05f43-645">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="05f43-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="05f43-646">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="05f43-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="05f43-647">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="05f43-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="05f43-648">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="05f43-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="05f43-649">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="05f43-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="05f43-650">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="05f43-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="05f43-651">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-651">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="05f43-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="05f43-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="05f43-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-657">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="05f43-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-658">Az.Sql</span></span>
* <span data-ttu-id="05f43-659">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="05f43-660">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="05f43-661">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="05f43-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="05f43-662">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="05f43-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="05f43-663">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="05f43-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="05f43-664">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="05f43-665">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="05f43-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="05f43-666">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="05f43-667">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="05f43-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-668">Az.Storage</span></span>
* <span data-ttu-id="05f43-669">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="05f43-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="05f43-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="05f43-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="05f43-672">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="05f43-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="05f43-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="05f43-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="05f43-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="05f43-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="05f43-675">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="05f43-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="05f43-676">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-676">General</span></span>
* <span data-ttu-id="05f43-677">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="05f43-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-678">Az.Accounts</span></span>
* <span data-ttu-id="05f43-679">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="05f43-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="05f43-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-680">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-681">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="05f43-682">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-683">Az.Automation</span></span>
* <span data-ttu-id="05f43-684">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="05f43-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-685">Az.Batch</span></span>
* <span data-ttu-id="05f43-686">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="05f43-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-687">Az.Compute</span></span>
* <span data-ttu-id="05f43-688">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="05f43-689">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="05f43-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="05f43-690">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="05f43-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="05f43-691">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="05f43-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-692">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-693">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="05f43-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="05f43-694">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="05f43-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="05f43-695">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="05f43-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-697">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="05f43-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="05f43-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="05f43-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="05f43-699">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="05f43-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="05f43-700">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="05f43-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="05f43-701">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="05f43-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="05f43-702">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="05f43-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-703">Az.IotHub</span></span>
* <span data-ttu-id="05f43-704">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="05f43-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="05f43-705">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="05f43-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-706">Az.Monitor</span></span>
* <span data-ttu-id="05f43-707">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="05f43-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="05f43-708">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="05f43-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="05f43-709">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="05f43-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="05f43-710">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="05f43-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-711">Az.Network</span></span>
* <span data-ttu-id="05f43-712">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="05f43-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="05f43-713">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="05f43-714">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-714">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="05f43-716">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="05f43-717">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="05f43-718">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="05f43-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="05f43-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="05f43-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="05f43-722">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="05f43-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="05f43-723">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="05f43-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="05f43-724">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="05f43-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="05f43-725">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="05f43-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="05f43-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="05f43-726">Az.RedisCache</span></span>
* <span data-ttu-id="05f43-727">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="05f43-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-728">Az.Sql</span></span>
* <span data-ttu-id="05f43-729">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-730">Az.Storage</span></span>
* <span data-ttu-id="05f43-731">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="05f43-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="05f43-732">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="05f43-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="05f43-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="05f43-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="05f43-734">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="05f43-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="05f43-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="05f43-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="05f43-736">Az.StorageSync</span></span>
* <span data-ttu-id="05f43-737">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="05f43-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-738">Az.Websites</span></span>
* <span data-ttu-id="05f43-739">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="05f43-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="05f43-740">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="05f43-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="05f43-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-741">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-742">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="05f43-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="05f43-743">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="05f43-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="05f43-744">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="05f43-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-745">Az.Automation</span></span>
* <span data-ttu-id="05f43-746">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="05f43-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="05f43-747">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="05f43-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="05f43-748">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05f43-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-749">Az.Compute</span></span>
* <span data-ttu-id="05f43-750">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="05f43-751">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="05f43-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="05f43-752">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="05f43-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="05f43-753">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="05f43-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="05f43-754">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="05f43-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="05f43-755">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="05f43-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="05f43-756">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05f43-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="05f43-757">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="05f43-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="05f43-758">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-759">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-760">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="05f43-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="05f43-761">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="05f43-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="05f43-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-762">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-763">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="05f43-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-764">Az.IotHub</span></span>
* <span data-ttu-id="05f43-765">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="05f43-766">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="05f43-767">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="05f43-767">New cmdlets are:</span></span>
    - <span data-ttu-id="05f43-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="05f43-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="05f43-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="05f43-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="05f43-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="05f43-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="05f43-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="05f43-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-772">Az.Monitor</span></span>
* <span data-ttu-id="05f43-773">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="05f43-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="05f43-774">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="05f43-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="05f43-775">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="05f43-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="05f43-776">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="05f43-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="05f43-777">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="05f43-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="05f43-778">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="05f43-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="05f43-779">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="05f43-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="05f43-780">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="05f43-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="05f43-781">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="05f43-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="05f43-782">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="05f43-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="05f43-783">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="05f43-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="05f43-784">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="05f43-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="05f43-785">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="05f43-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="05f43-786">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="05f43-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="05f43-787">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="05f43-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="05f43-788">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="05f43-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="05f43-789">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="05f43-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="05f43-790">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="05f43-791">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="05f43-792">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="05f43-792">Overall improved help files</span></span>
* <span data-ttu-id="05f43-793">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-794">Az.Network</span></span>
* <span data-ttu-id="05f43-795">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="05f43-796">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="05f43-797">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="05f43-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="05f43-798">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="05f43-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="05f43-799">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="05f43-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="05f43-800">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="05f43-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="05f43-801">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="05f43-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="05f43-802">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="05f43-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="05f43-803">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="05f43-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="05f43-804">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="05f43-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="05f43-805">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="05f43-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="05f43-806">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="05f43-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="05f43-807">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-807">New cmdlets</span></span>
        - <span data-ttu-id="05f43-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="05f43-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="05f43-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="05f43-810">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="05f43-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="05f43-811">New-VpnSite</span></span>
        - <span data-ttu-id="05f43-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="05f43-812">Update-VpnSite</span></span>
        - <span data-ttu-id="05f43-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-813">New-VpnConnection</span></span>
        - <span data-ttu-id="05f43-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-814">Update-VpnConnection</span></span>
* <span data-ttu-id="05f43-815">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-817">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="05f43-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="05f43-818">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="05f43-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-819">Az.Resources</span></span>
* <span data-ttu-id="05f43-820">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="05f43-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-822">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="05f43-823">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="05f43-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="05f43-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="05f43-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="05f43-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="05f43-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="05f43-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="05f43-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="05f43-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="05f43-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="05f43-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="05f43-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="05f43-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="05f43-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="05f43-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="05f43-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="05f43-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="05f43-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="05f43-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="05f43-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="05f43-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="05f43-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="05f43-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="05f43-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="05f43-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="05f43-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="05f43-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="05f43-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="05f43-837">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="05f43-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="05f43-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="05f43-838">Az.SignalR</span></span>
* <span data-ttu-id="05f43-839">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-840">Az.Sql</span></span>
* <span data-ttu-id="05f43-841">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="05f43-842">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="05f43-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="05f43-843">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="05f43-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="05f43-844">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="05f43-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="05f43-845">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="05f43-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-846">Az.Storage</span></span>
* <span data-ttu-id="05f43-847">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="05f43-848">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="05f43-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="05f43-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05f43-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="05f43-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05f43-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="05f43-851">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="05f43-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="05f43-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="05f43-853">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="05f43-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="05f43-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="05f43-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="05f43-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="05f43-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="05f43-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-858">Az.Websites</span></span>
* <span data-ttu-id="05f43-859">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="05f43-860">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="05f43-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="05f43-861">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="05f43-862">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="05f43-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="05f43-863">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-863">General</span></span>
* <span data-ttu-id="05f43-864">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="05f43-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-865">Az.Accounts</span></span>
* <span data-ttu-id="05f43-866">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="05f43-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="05f43-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="05f43-867">Az.Aks</span></span>
* <span data-ttu-id="05f43-868">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="05f43-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="05f43-869">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="05f43-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="05f43-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-870">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-871">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="05f43-872">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="05f43-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="05f43-873">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="05f43-874">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="05f43-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="05f43-875">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="05f43-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="05f43-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-876">Az.Batch</span></span>
* <span data-ttu-id="05f43-877">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="05f43-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-878">Az.Cdn</span></span>
* <span data-ttu-id="05f43-879">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-880">Az.Compute</span></span>
* <span data-ttu-id="05f43-881">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="05f43-882">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="05f43-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="05f43-883">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="05f43-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="05f43-884">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="05f43-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="05f43-885">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="05f43-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="05f43-886">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="05f43-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="05f43-887">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="05f43-888">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="05f43-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-889">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-890">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="05f43-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="05f43-891">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="05f43-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="05f43-892">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="05f43-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="05f43-893">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="05f43-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-895">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05f43-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-896">Az.EventHub</span></span>
* <span data-ttu-id="05f43-897">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="05f43-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="05f43-898">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="05f43-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="05f43-899">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="05f43-900">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="05f43-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="05f43-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="05f43-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="05f43-902">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="05f43-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-903">Az.Monitor</span></span>
* <span data-ttu-id="05f43-904">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-905">Az.Network</span></span>
* <span data-ttu-id="05f43-906">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="05f43-907">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="05f43-908">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="05f43-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="05f43-909">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="05f43-910">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="05f43-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="05f43-911">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="05f43-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="05f43-912">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="05f43-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-914">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="05f43-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="05f43-915">新增了範例</span><span class="sxs-lookup"><span data-stu-id="05f43-915">Added example</span></span>
    - <span data-ttu-id="05f43-916">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="05f43-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="05f43-917">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="05f43-918">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="05f43-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-920">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-921">Az.Resources</span></span>
* <span data-ttu-id="05f43-922">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="05f43-923">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="05f43-924">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="05f43-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="05f43-925">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="05f43-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-926">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-927">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="05f43-928">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="05f43-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="05f43-929">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="05f43-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-931">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="05f43-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="05f43-932">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="05f43-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="05f43-933">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="05f43-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="05f43-934">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="05f43-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="05f43-935">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="05f43-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="05f43-936">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-937">Az.Sql</span></span>
* <span data-ttu-id="05f43-938">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="05f43-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-939">Az.Storage</span></span>
* <span data-ttu-id="05f43-940">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="05f43-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="05f43-941">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="05f43-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="05f43-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="05f43-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="05f43-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="05f43-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="05f43-944">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="05f43-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="05f43-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="05f43-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-946">Az.Websites</span></span>
* <span data-ttu-id="05f43-947">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="05f43-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="05f43-948">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="05f43-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-949">Az.Accounts</span></span>
* <span data-ttu-id="05f43-950">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="05f43-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="05f43-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="05f43-952">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-953">Az.Automation</span></span>
* <span data-ttu-id="05f43-954">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-956">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-957">Az.Compute</span></span>
* <span data-ttu-id="05f43-958">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="05f43-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="05f43-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05f43-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="05f43-960">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="05f43-961">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="05f43-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-962">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-963">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="05f43-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="05f43-964">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-965">Az.EventHub</span></span>
* <span data-ttu-id="05f43-966">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="05f43-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="05f43-967">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-968">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-969">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="05f43-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="05f43-970">Az.LogicApp</span></span>
* <span data-ttu-id="05f43-971">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="05f43-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="05f43-972">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="05f43-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="05f43-973">Az.ManagedServices</span></span>
* <span data-ttu-id="05f43-974">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-975">Az.Network</span></span>
* <span data-ttu-id="05f43-976">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="05f43-977">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-977">New cmdlets</span></span>
        - <span data-ttu-id="05f43-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05f43-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="05f43-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="05f43-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="05f43-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="05f43-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="05f43-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="05f43-986">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="05f43-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="05f43-987">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="05f43-988">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="05f43-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="05f43-989">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="05f43-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="05f43-990">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="05f43-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="05f43-991">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="05f43-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="05f43-992">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-992">Updated cmdlets</span></span>
        - <span data-ttu-id="05f43-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="05f43-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="05f43-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="05f43-996">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="05f43-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="05f43-997">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="05f43-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="05f43-998">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="05f43-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="05f43-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="05f43-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="05f43-1002">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="05f43-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="05f43-1003">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="05f43-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="05f43-1004">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="05f43-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-1006">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="05f43-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="05f43-1007">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="05f43-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1009">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="05f43-1010">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="05f43-1011">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="05f43-1012">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="05f43-1013">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="05f43-1014">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="05f43-1015">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="05f43-1016">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="05f43-1017">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="05f43-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="05f43-1018">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="05f43-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1019">Az.Resources</span></span>
- <span data-ttu-id="05f43-1020">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="05f43-1021">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="05f43-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-1023">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="05f43-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="05f43-1024">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1025">Az.Sql</span></span>
* <span data-ttu-id="05f43-1026">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="05f43-1027">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="05f43-1028">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="05f43-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1029">Az.Storage</span></span>
* <span data-ttu-id="05f43-1030">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="05f43-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="05f43-1031">Az.StorageSync</span></span>
* <span data-ttu-id="05f43-1032">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="05f43-1033">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="05f43-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1034">Az.Websites</span></span>
* <span data-ttu-id="05f43-1035">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="05f43-1036">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="05f43-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="05f43-1037">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="05f43-1038">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1039">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1040">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="05f43-1041">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="05f43-1042">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="05f43-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="05f43-1043">Az.Advisor</span></span>
* <span data-ttu-id="05f43-1044">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="05f43-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="05f43-1045">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="05f43-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="05f43-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-1047">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="05f43-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="05f43-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="05f43-1049">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="05f43-1050">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="05f43-1051">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="05f43-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="05f43-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="05f43-1053">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1054">Az.Automation</span></span>
* <span data-ttu-id="05f43-1055">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="05f43-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1056">Az.Compute</span></span>
* <span data-ttu-id="05f43-1057">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-1058">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-1059">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="05f43-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="05f43-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="05f43-1060">Az.EventGrid</span></span>
* <span data-ttu-id="05f43-1061">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1062">Az.IotHub</span></span>
* <span data-ttu-id="05f43-1063">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1064">Az.Network</span></span>
* <span data-ttu-id="05f43-1065">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="05f43-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="05f43-1066">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="05f43-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="05f43-1068">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="05f43-1069">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="05f43-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-1071">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="05f43-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1073">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="05f43-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1074">Az.Resources</span></span>
    - <span data-ttu-id="05f43-1075">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="05f43-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="05f43-1076">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="05f43-1077">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="05f43-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="05f43-1078">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="05f43-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-1080">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="05f43-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1081">Az.Sql</span></span>
* <span data-ttu-id="05f43-1082">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="05f43-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="05f43-1083">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="05f43-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="05f43-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="05f43-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="05f43-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="05f43-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="05f43-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="05f43-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="05f43-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="05f43-1090">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="05f43-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1091">Az.Storage</span></span>
* <span data-ttu-id="05f43-1092">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="05f43-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="05f43-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="05f43-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="05f43-1094">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="05f43-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="05f43-1095">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="05f43-1096">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="05f43-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="05f43-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="05f43-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="05f43-1099">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="05f43-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="05f43-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="05f43-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="05f43-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="05f43-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="05f43-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="05f43-1102">Az.StorageSync</span></span>
* <span data-ttu-id="05f43-1103">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="05f43-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="05f43-1104">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1105">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1106">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="05f43-1107">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="05f43-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="05f43-1108">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="05f43-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="05f43-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="05f43-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="05f43-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1111">Az.Compute</span></span>
* <span data-ttu-id="05f43-1112">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="05f43-1113">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="05f43-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="05f43-1114">Az.Dns</span></span>
* <span data-ttu-id="05f43-1115">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="05f43-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="05f43-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="05f43-1116">Az.EventGrid</span></span>
* <span data-ttu-id="05f43-1117">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="05f43-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="05f43-1118">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1118">New cmdlets:</span></span>
    - <span data-ttu-id="05f43-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="05f43-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="05f43-1120">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="05f43-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="05f43-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="05f43-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="05f43-1122">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="05f43-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="05f43-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="05f43-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="05f43-1124">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="05f43-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="05f43-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="05f43-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="05f43-1126">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="05f43-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="05f43-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="05f43-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="05f43-1128">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="05f43-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="05f43-1129">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="05f43-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="05f43-1130">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="05f43-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="05f43-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="05f43-1132">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="05f43-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="05f43-1133">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="05f43-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="05f43-1134">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="05f43-1135">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="05f43-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="05f43-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="05f43-1137">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="05f43-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="05f43-1138">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="05f43-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="05f43-1139">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="05f43-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="05f43-1140">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="05f43-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="05f43-1141">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="05f43-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="05f43-1142">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="05f43-1143">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="05f43-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="05f43-1144">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="05f43-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="05f43-1145">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="05f43-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="05f43-1146">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="05f43-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="05f43-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="05f43-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="05f43-1148">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="05f43-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="05f43-1149">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="05f43-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="05f43-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="05f43-1152">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="05f43-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="05f43-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="05f43-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="05f43-1154">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="05f43-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1155">Az.Network</span></span>
* <span data-ttu-id="05f43-1156">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="05f43-1157">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1157">New cmdlets</span></span>
        - <span data-ttu-id="05f43-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="05f43-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="05f43-1159">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="05f43-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="05f43-1160">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1160">New cmdlets</span></span>
        - <span data-ttu-id="05f43-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="05f43-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="05f43-1162">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="05f43-1163">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1163">New cmdlets</span></span>
        - <span data-ttu-id="05f43-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="05f43-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="05f43-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="05f43-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="05f43-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="05f43-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="05f43-1169">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05f43-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="05f43-1170">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1170">New cmdlets</span></span>
        - <span data-ttu-id="05f43-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05f43-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="05f43-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05f43-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="05f43-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="05f43-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="05f43-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="05f43-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="05f43-1175">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="05f43-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="05f43-1176">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="05f43-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="05f43-1177">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="05f43-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="05f43-1178">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="05f43-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="05f43-1179">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="05f43-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="05f43-1180">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="05f43-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="05f43-1181">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="05f43-1182">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="05f43-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="05f43-1183">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="05f43-1184">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="05f43-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="05f43-1185">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="05f43-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="05f43-1186">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="05f43-1187">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="05f43-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="05f43-1188">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="05f43-1189">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="05f43-1190">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="05f43-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="05f43-1191">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="05f43-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="05f43-1192">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="05f43-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="05f43-1193">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="05f43-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="05f43-1194">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="05f43-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="05f43-1195">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="05f43-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="05f43-1196">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="05f43-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="05f43-1197">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="05f43-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-1199">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="05f43-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1200">Az.Resources</span></span>
* <span data-ttu-id="05f43-1201">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="05f43-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="05f43-1202">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="05f43-1203">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="05f43-1204">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="05f43-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-1206">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1207">Az.Sql</span></span>
* <span data-ttu-id="05f43-1208">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="05f43-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="05f43-1209">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="05f43-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="05f43-1210">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="05f43-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="05f43-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="05f43-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="05f43-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="05f43-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="05f43-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="05f43-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="05f43-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="05f43-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="05f43-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="05f43-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1216">Az.Storage</span></span>
* <span data-ttu-id="05f43-1217">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="05f43-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="05f43-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="05f43-1219">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="05f43-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="05f43-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1221">Az.Websites</span></span>
* <span data-ttu-id="05f43-1222">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="05f43-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="05f43-1223">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="05f43-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="05f43-1224">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="05f43-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-1225">Az.Cdn</span></span>
* <span data-ttu-id="05f43-1226">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="05f43-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1227">Az.Compute</span></span>
* <span data-ttu-id="05f43-1228">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="05f43-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="05f43-1229">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="05f43-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1230">Az.EventHub</span></span>
* <span data-ttu-id="05f43-1231">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="05f43-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="05f43-1232">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f43-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1233">Az.Network</span></span>
* <span data-ttu-id="05f43-1234">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="05f43-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="05f43-1235">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="05f43-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="05f43-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="05f43-1237">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1239">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="05f43-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-1241">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f43-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-1243">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="05f43-1244">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1245">Az.Sql</span></span>
* <span data-ttu-id="05f43-1246">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="05f43-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="05f43-1247">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="05f43-1248">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="05f43-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="05f43-1249">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1250">Az.Websites</span></span>
* <span data-ttu-id="05f43-1251">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="05f43-1252">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="05f43-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-1254">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="05f43-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="05f43-1255">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="05f43-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="05f43-1256">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="05f43-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="05f43-1257">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="05f43-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="05f43-1258">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="05f43-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="05f43-1259">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="05f43-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="05f43-1260">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="05f43-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="05f43-1261">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="05f43-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="05f43-1262">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="05f43-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="05f43-1263">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="05f43-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="05f43-1264">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="05f43-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="05f43-1265">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="05f43-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="05f43-1266">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="05f43-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="05f43-1267">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="05f43-1268">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="05f43-1269">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="05f43-1270">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="05f43-1271">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="05f43-1272">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="05f43-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="05f43-1273">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="05f43-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="05f43-1274">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="05f43-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="05f43-1275">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="05f43-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="05f43-1276">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="05f43-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="05f43-1277">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="05f43-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="05f43-1278">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="05f43-1279">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="05f43-1280">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="05f43-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="05f43-1281">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="05f43-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="05f43-1282">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="05f43-1283">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="05f43-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="05f43-1284">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="05f43-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="05f43-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="05f43-1286">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="05f43-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="05f43-1287">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="05f43-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="05f43-1288">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="05f43-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="05f43-1289">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="05f43-1290">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="05f43-1291">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="05f43-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="05f43-1292">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="05f43-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="05f43-1293">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="05f43-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="05f43-1294">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="05f43-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="05f43-1295">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="05f43-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="05f43-1296">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="05f43-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="05f43-1297">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="05f43-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="05f43-1298">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="05f43-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="05f43-1299">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="05f43-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="05f43-1300">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="05f43-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="05f43-1301">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="05f43-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="05f43-1302">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="05f43-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="05f43-1303">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="05f43-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="05f43-1304">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="05f43-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="05f43-1305">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="05f43-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="05f43-1306">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="05f43-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="05f43-1307">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="05f43-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="05f43-1308">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="05f43-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="05f43-1309">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="05f43-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="05f43-1310">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="05f43-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="05f43-1311">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="05f43-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="05f43-1312">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="05f43-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="05f43-1313">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="05f43-1314">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="05f43-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="05f43-1315">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="05f43-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="05f43-1316">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="05f43-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="05f43-1317">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="05f43-1318">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="05f43-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="05f43-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="05f43-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="05f43-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="05f43-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="05f43-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="05f43-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="05f43-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="05f43-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="05f43-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="05f43-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="05f43-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="05f43-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="05f43-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="05f43-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="05f43-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="05f43-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="05f43-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="05f43-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="05f43-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="05f43-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="05f43-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="05f43-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="05f43-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1331">Az.Automation</span></span>
* <span data-ttu-id="05f43-1332">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="05f43-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="05f43-1333">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="05f43-1334">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="05f43-1335">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="05f43-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="05f43-1336">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="05f43-1337">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="05f43-1338">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="05f43-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1339">Az.Compute</span></span>
* <span data-ttu-id="05f43-1340">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="05f43-1341">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="05f43-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-1343">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="05f43-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-1344">Az.Monitor</span></span>
* <span data-ttu-id="05f43-1345">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1346">Az.Network</span></span>
* <span data-ttu-id="05f43-1347">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="05f43-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="05f43-1348">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="05f43-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="05f43-1350">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="05f43-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1351">Az.Resources</span></span>
* <span data-ttu-id="05f43-1352">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="05f43-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1353">Az.Sql</span></span>
* <span data-ttu-id="05f43-1354">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="05f43-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="05f43-1355">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1356">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1357">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-1359">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="05f43-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="05f43-1360">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="05f43-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1361">Az.Compute</span></span>
* <span data-ttu-id="05f43-1362">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="05f43-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="05f43-1363">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="05f43-1364">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="05f43-1365">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="05f43-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="05f43-1366">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="05f43-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="05f43-1367">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="05f43-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="05f43-1368">重大變更</span><span class="sxs-lookup"><span data-stu-id="05f43-1368">Breaking changes</span></span>
    - <span data-ttu-id="05f43-1369">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="05f43-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="05f43-1370">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="05f43-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="05f43-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="05f43-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="05f43-1372">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="05f43-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="05f43-1373">Az.Dns</span></span>
* <span data-ttu-id="05f43-1374">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="05f43-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="05f43-1375">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="05f43-1376">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="05f43-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="05f43-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="05f43-1378">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="05f43-1379">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="05f43-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="05f43-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-1380">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-1381">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="05f43-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="05f43-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="05f43-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="05f43-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="05f43-1384">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="05f43-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="05f43-1385">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="05f43-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="05f43-1386">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="05f43-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="05f43-1387">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="05f43-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-1388">Az.Monitor</span></span>
* <span data-ttu-id="05f43-1389">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="05f43-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="05f43-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="05f43-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="05f43-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="05f43-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="05f43-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="05f43-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="05f43-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="05f43-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="05f43-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="05f43-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="05f43-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="05f43-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="05f43-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="05f43-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="05f43-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="05f43-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="05f43-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="05f43-1401">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="05f43-1402">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1403">Az.Network</span></span>
* <span data-ttu-id="05f43-1404">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="05f43-1405">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1405">New cmdlets</span></span>
        - <span data-ttu-id="05f43-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="05f43-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="05f43-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="05f43-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="05f43-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="05f43-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="05f43-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="05f43-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="05f43-1410">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="05f43-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="05f43-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="05f43-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="05f43-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="05f43-1413">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="05f43-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="05f43-1414">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="05f43-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="05f43-1415">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="05f43-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="05f43-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="05f43-1417">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="05f43-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="05f43-1418">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="05f43-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="05f43-1419">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="05f43-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1421">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="05f43-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="05f43-1422">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="05f43-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="05f43-1423">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="05f43-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="05f43-1424">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="05f43-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="05f43-1425">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="05f43-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="05f43-1426">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="05f43-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="05f43-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="05f43-1427">Az.Relay</span></span>
* <span data-ttu-id="05f43-1428">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-1430">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1431">Az.Storage</span></span>
* <span data-ttu-id="05f43-1432">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="05f43-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="05f43-1433">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="05f43-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="05f43-1434">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="05f43-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="05f43-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="05f43-1436">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="05f43-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="05f43-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="05f43-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="05f43-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1440">Az.Websites</span></span>
* <span data-ttu-id="05f43-1441">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="05f43-1442">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="05f43-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="05f43-1443">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-1444">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-1445">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="05f43-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="05f43-1446">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="05f43-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="05f43-1447">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="05f43-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="05f43-1448">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="05f43-1449">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="05f43-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="05f43-1450">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="05f43-1451">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1452">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1453">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="05f43-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="05f43-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-1454">Az.Batch</span></span>
* <span data-ttu-id="05f43-1455">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-1456">Az.Cdn</span></span>
* <span data-ttu-id="05f43-1457">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-1459">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1460">Az.Compute</span></span>
* <span data-ttu-id="05f43-1461">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="05f43-1462">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1463">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-1464">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-1465">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="05f43-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-1467">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="05f43-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="05f43-1468">Az.EventGrid</span></span>
* <span data-ttu-id="05f43-1469">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1470">Az.EventHub</span></span>
* <span data-ttu-id="05f43-1471">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="05f43-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="05f43-1472">Az.HDInsight</span></span>
* <span data-ttu-id="05f43-1473">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1474">Az.IotHub</span></span>
* <span data-ttu-id="05f43-1475">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-1476">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-1477">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1478">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="05f43-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="05f43-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="05f43-1480">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="05f43-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="05f43-1481">Az.Media</span></span>
* <span data-ttu-id="05f43-1482">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-1483">Az.Monitor</span></span>
  * <span data-ttu-id="05f43-1484">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="05f43-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="05f43-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="05f43-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="05f43-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="05f43-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="05f43-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="05f43-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="05f43-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="05f43-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="05f43-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="05f43-1490">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="05f43-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1491">Az.Network</span></span>
* <span data-ttu-id="05f43-1492">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1493">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="05f43-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="05f43-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="05f43-1495">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-1497">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="05f43-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="05f43-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="05f43-1499">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1501">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1502">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="05f43-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="05f43-1503">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="05f43-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="05f43-1504">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="05f43-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="05f43-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="05f43-1505">Az.RedisCache</span></span>
* <span data-ttu-id="05f43-1506">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1507">Az.Resources</span></span>
* <span data-ttu-id="05f43-1508">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1509">Az.Sql</span></span>
* <span data-ttu-id="05f43-1510">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="05f43-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="05f43-1511">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1512">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="05f43-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="05f43-1513">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="05f43-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="05f43-1514">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="05f43-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="05f43-1515">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="05f43-1516">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="05f43-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1517">Az.Websites</span></span>
* <span data-ttu-id="05f43-1518">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="05f43-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="05f43-1519">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="05f43-1520">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="05f43-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="05f43-1521">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="05f43-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="05f43-1522">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-1523">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-1524">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="05f43-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="05f43-1525">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="05f43-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="05f43-1526">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="05f43-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="05f43-1527">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="05f43-1528">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="05f43-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="05f43-1529">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="05f43-1530">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="05f43-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1531">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1532">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="05f43-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="05f43-1534">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="05f43-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="05f43-1535">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="05f43-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1536">Az.Automation</span></span>
* <span data-ttu-id="05f43-1537">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="05f43-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="05f43-1538">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="05f43-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="05f43-1539">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="05f43-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1540">Az.Compute</span></span>
* <span data-ttu-id="05f43-1541">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="05f43-1542">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="05f43-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="05f43-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="05f43-1544">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="05f43-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-1545">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-1546">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="05f43-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="05f43-1547">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1548">Az.Resources</span></span>
* <span data-ttu-id="05f43-1549">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="05f43-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="05f43-1550">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="05f43-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="05f43-1551">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="05f43-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="05f43-1552">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="05f43-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="05f43-1553">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="05f43-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="05f43-1554">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="05f43-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1555">Az.Sql</span></span>
* <span data-ttu-id="05f43-1556">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="05f43-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1557">Az.Storage</span></span>
* <span data-ttu-id="05f43-1558">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="05f43-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="05f43-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="05f43-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="05f43-1560">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="05f43-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="05f43-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="05f43-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="05f43-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="05f43-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="05f43-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="05f43-1565">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="05f43-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="05f43-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="05f43-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="05f43-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="05f43-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05f43-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="05f43-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="05f43-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="05f43-1570">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="05f43-1571">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="05f43-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="05f43-1572">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="05f43-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="05f43-1573">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="05f43-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="05f43-1574">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="05f43-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="05f43-1575">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="05f43-1576">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="05f43-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="05f43-1577">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="05f43-1578">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1579">Az.Automation</span></span>
* <span data-ttu-id="05f43-1580">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="05f43-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="05f43-1581">動態分組</span><span class="sxs-lookup"><span data-stu-id="05f43-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="05f43-1582">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="05f43-1582">Pre-Post script</span></span>
    * <span data-ttu-id="05f43-1583">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="05f43-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1584">Az.Compute</span></span>
* <span data-ttu-id="05f43-1585">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="05f43-1586">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="05f43-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-1587">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-1588">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1589">Az.Network</span></span>
* <span data-ttu-id="05f43-1590">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="05f43-1591">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="05f43-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1593">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="05f43-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="05f43-1594">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1595">Az.Resources</span></span>
* <span data-ttu-id="05f43-1596">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="05f43-1597">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="05f43-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1598">Az.Sql</span></span>
* <span data-ttu-id="05f43-1599">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="05f43-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1600">Az.Storage</span></span>
* <span data-ttu-id="05f43-1601">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="05f43-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="05f43-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="05f43-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="05f43-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="05f43-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="05f43-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="05f43-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="05f43-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="05f43-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1608">Az.Websites</span></span>
* <span data-ttu-id="05f43-1609">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="05f43-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="05f43-1610">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1611">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1612">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="05f43-1613">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1614">Az.Automation</span></span>
* <span data-ttu-id="05f43-1615">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="05f43-1616">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="05f43-1617">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="05f43-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-1618">Az.Cdn</span></span>
* <span data-ttu-id="05f43-1619">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1620">Az.Compute</span></span>
* <span data-ttu-id="05f43-1621">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-1622">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-1623">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="05f43-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="05f43-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="05f43-1624">Az.LogicApp</span></span>
* <span data-ttu-id="05f43-1625">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="05f43-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1626">Az.Network</span></span>
* <span data-ttu-id="05f43-1627">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1629">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="05f43-1630">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="05f43-1630">SDK Update</span></span>
* <span data-ttu-id="05f43-1631">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="05f43-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="05f43-1632">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="05f43-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1633">Az.Resources</span></span>
* <span data-ttu-id="05f43-1634">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="05f43-1635">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="05f43-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="05f43-1636">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="05f43-1637">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="05f43-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="05f43-1638">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="05f43-1639">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="05f43-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1640">Az.Sql</span></span>
* <span data-ttu-id="05f43-1641">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="05f43-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="05f43-1642">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="05f43-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1643">Az.Storage</span></span>
* <span data-ttu-id="05f43-1644">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="05f43-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="05f43-1645">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="05f43-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="05f43-1647">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1648">Az.Automation</span></span>
* <span data-ttu-id="05f43-1649">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="05f43-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="05f43-1650">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="05f43-1651">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="05f43-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-1653">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="05f43-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1654">Az.Compute</span></span>
* <span data-ttu-id="05f43-1655">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="05f43-1656">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="05f43-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="05f43-1657">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="05f43-1658">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="05f43-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-1660">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="05f43-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1661">Az.EventHub</span></span>
* <span data-ttu-id="05f43-1662">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="05f43-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-1663">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-1664">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="05f43-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="05f43-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="05f43-1665">Az.LogicApp</span></span>
* <span data-ttu-id="05f43-1666">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="05f43-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="05f43-1667">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="05f43-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="05f43-1668">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="05f43-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="05f43-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="05f43-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="05f43-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="05f43-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="05f43-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="05f43-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="05f43-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="05f43-1673">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="05f43-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="05f43-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="05f43-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="05f43-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="05f43-1678">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="05f43-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="05f43-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-1679">Az.Monitor</span></span>
* <span data-ttu-id="05f43-1680">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="05f43-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1681">Az.Network</span></span>
* <span data-ttu-id="05f43-1682">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="05f43-1684">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="05f43-1685">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="05f43-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="05f43-1686">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="05f43-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1687">Az.Resources</span></span>
* <span data-ttu-id="05f43-1688">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="05f43-1689">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="05f43-1690">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="05f43-1691">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1692">Az.Sql</span></span>
* <span data-ttu-id="05f43-1693">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="05f43-1694">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="05f43-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1695">Az.Websites</span></span>
* <span data-ttu-id="05f43-1696">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="05f43-1697">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1698">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1699">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="05f43-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="05f43-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="05f43-1701">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="05f43-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1702">Az.Compute</span></span>
* <span data-ttu-id="05f43-1703">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="05f43-1704">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="05f43-1705">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="05f43-1707">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="05f43-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1708">Az.Resources</span></span>
* <span data-ttu-id="05f43-1709">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="05f43-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="05f43-1710">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="05f43-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="05f43-1711">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="05f43-1712">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="05f43-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1713">Az.Sql</span></span>
* <span data-ttu-id="05f43-1714">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="05f43-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="05f43-1715">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="05f43-1716">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="05f43-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="05f43-1717">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1718">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1719">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="05f43-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="05f43-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="05f43-1721">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="05f43-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="05f43-1723">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="05f43-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="05f43-1724">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1725">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1726">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="05f43-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="05f43-1727">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="05f43-1728">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="05f43-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="05f43-1729">Az.Aks</span></span>
* <span data-ttu-id="05f43-1730">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="05f43-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1731">Az.Automation</span></span>
* <span data-ttu-id="05f43-1732">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="05f43-1733">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="05f43-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="05f43-1734">Az.Cdn</span></span>
* <span data-ttu-id="05f43-1735">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1736">Az.Compute</span></span>
* <span data-ttu-id="05f43-1737">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="05f43-1738">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="05f43-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="05f43-1739">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="05f43-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="05f43-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="05f43-1741">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="05f43-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="05f43-1742">Az.DataFactory</span></span>
* <span data-ttu-id="05f43-1743">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="05f43-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-1745">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="05f43-1746">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="05f43-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="05f43-1747">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1748">Az.IotHub</span></span>
* <span data-ttu-id="05f43-1749">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="05f43-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-1750">Az.KeyVault</span></span>
* <span data-ttu-id="05f43-1751">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1752">Az.Network</span></span>
* <span data-ttu-id="05f43-1753">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1754">Az.Resources</span></span>
* <span data-ttu-id="05f43-1755">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="05f43-1756">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="05f43-1757">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="05f43-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="05f43-1758">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="05f43-1759">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="05f43-1760">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="05f43-1761">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="05f43-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-1763">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="05f43-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="05f43-1764">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="05f43-1764">Fix some error messages.</span></span>
* <span data-ttu-id="05f43-1765">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="05f43-1766">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="05f43-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="05f43-1767">Az.SignalR</span></span>
* <span data-ttu-id="05f43-1768">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1769">Az.Sql</span></span>
* <span data-ttu-id="05f43-1770">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="05f43-1771">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="05f43-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="05f43-1772">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="05f43-1773">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="05f43-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1774">Az.Storage</span></span>
* <span data-ttu-id="05f43-1775">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="05f43-1776">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="05f43-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="05f43-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="05f43-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="05f43-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="05f43-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="05f43-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="05f43-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="05f43-1780">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1781">Az.Websites</span></span>
* <span data-ttu-id="05f43-1782">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="05f43-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="05f43-1783">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="05f43-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="05f43-1784">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="05f43-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="05f43-1785">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="05f43-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1786">Az.Accounts</span></span>
* <span data-ttu-id="05f43-1787">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="05f43-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1788">Az.Compute</span></span>
* <span data-ttu-id="05f43-1789">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="05f43-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="05f43-1790">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="05f43-1791">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-1793">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="05f43-1794">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="05f43-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="05f43-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="05f43-1795">Az.EventGrid</span></span>
* <span data-ttu-id="05f43-1796">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="05f43-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="05f43-1797">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="05f43-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="05f43-1798">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="05f43-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="05f43-1799">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="05f43-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="05f43-1800">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="05f43-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="05f43-1801">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="05f43-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="05f43-1802">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="05f43-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="05f43-1803">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="05f43-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="05f43-1804">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="05f43-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="05f43-1805">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="05f43-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="05f43-1806">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="05f43-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="05f43-1807">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="05f43-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="05f43-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="05f43-1808">Az.IotHub</span></span>
* <span data-ttu-id="05f43-1809">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="05f43-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="05f43-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="05f43-1810">Az.LogicApp</span></span>
* <span data-ttu-id="05f43-1811">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1812">Az.Resources</span></span>
* <span data-ttu-id="05f43-1813">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="05f43-1814">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="05f43-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="05f43-1815">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="05f43-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="05f43-1816">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="05f43-1817">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="05f43-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="05f43-1818">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="05f43-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="05f43-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="05f43-1819">Az.SignalR</span></span>
* <span data-ttu-id="05f43-1820">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1821">Az.Sql</span></span>
* <span data-ttu-id="05f43-1822">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="05f43-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="05f43-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1823">Az.Storage</span></span>
* <span data-ttu-id="05f43-1824">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="05f43-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="05f43-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="05f43-1826">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="05f43-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="05f43-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="05f43-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1828">Az.Websites</span></span>
* <span data-ttu-id="05f43-1829">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="05f43-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="05f43-1830">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="05f43-1831">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="05f43-1832">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-1832">General</span></span>

- <span data-ttu-id="05f43-1833">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="05f43-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="05f43-1834">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="05f43-1834">Online help for each module</span></span>
- <span data-ttu-id="05f43-1835">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="05f43-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="05f43-1836">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="05f43-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1837">Az.Accounts</span></span>
- <span data-ttu-id="05f43-1838">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="05f43-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="05f43-1839">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="05f43-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="05f43-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="05f43-1841">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="05f43-1841">Fixes for #7002</span></span>
- <span data-ttu-id="05f43-1842">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="05f43-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="05f43-1843">Az.Batch</span></span>
- <span data-ttu-id="05f43-1844">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="05f43-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="05f43-1845">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="05f43-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="05f43-1846">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="05f43-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="05f43-1847">Az.Billing</span></span>
- <span data-ttu-id="05f43-1848">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="05f43-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="05f43-1850">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="05f43-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="05f43-1851">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="05f43-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="05f43-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="05f43-1853">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="05f43-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="05f43-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="05f43-1855">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="05f43-1857">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="05f43-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="05f43-1858">Az.Monitor</span></span>
- <span data-ttu-id="05f43-1859">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="05f43-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="05f43-1860">Az.KeyVault</span></span>
- <span data-ttu-id="05f43-1861">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="05f43-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="05f43-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="05f43-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="05f43-1863">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="05f43-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="05f43-1864">Az.Media</span></span>
- <span data-ttu-id="05f43-1865">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="05f43-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="05f43-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1866">Az.Network</span></span>
<span data-ttu-id="05f43-1867">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="05f43-1868">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="05f43-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="05f43-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="05f43-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="05f43-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="05f43-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="05f43-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="05f43-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="05f43-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05f43-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="05f43-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="05f43-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="05f43-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="05f43-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="05f43-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="05f43-1883">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="05f43-1884">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="05f43-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="05f43-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="05f43-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="05f43-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="05f43-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="05f43-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="05f43-1888">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="05f43-1889">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="05f43-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="05f43-1891">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="05f43-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="05f43-1892">Az.Profile</span></span>
- <span data-ttu-id="05f43-1893">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="05f43-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="05f43-1895">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="05f43-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1896">Az.Resources</span></span>
- <span data-ttu-id="05f43-1897">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="05f43-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="05f43-1899">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="05f43-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="05f43-1900">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="05f43-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="05f43-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="05f43-1902">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="05f43-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="05f43-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1903">Az.Sql</span></span>
- <span data-ttu-id="05f43-1904">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="05f43-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="05f43-1905">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="05f43-1906">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="05f43-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1907">Az.Storage</span></span>
- <span data-ttu-id="05f43-1908">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="05f43-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1909">Az.Websites</span></span>
- <span data-ttu-id="05f43-1910">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="05f43-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="05f43-1911">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="05f43-1912">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-1912">General</span></span>

* <span data-ttu-id="05f43-1913">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="05f43-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="05f43-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1914">Az.Compute</span></span>

* <span data-ttu-id="05f43-1915">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="05f43-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="05f43-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="05f43-1917">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="05f43-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="05f43-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="05f43-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="05f43-1919">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="05f43-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="05f43-1920">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="05f43-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="05f43-1921">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="05f43-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="05f43-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="05f43-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="05f43-1923">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="05f43-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="05f43-1924">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="05f43-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="05f43-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1925">Az.Resources</span></span>

* <span data-ttu-id="05f43-1926">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="05f43-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="05f43-1927">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="05f43-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="05f43-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1928">Az.Sql</span></span>

* <span data-ttu-id="05f43-1929">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="05f43-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="05f43-1930">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="05f43-1931">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="05f43-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="05f43-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-1932">Az.Storage</span></span>

* <span data-ttu-id="05f43-1933">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="05f43-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="05f43-1934">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="05f43-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="05f43-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="05f43-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="05f43-1936">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="05f43-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="05f43-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="05f43-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="05f43-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="05f43-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="05f43-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-1939">Az.Websites</span></span>

* <span data-ttu-id="05f43-1940">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="05f43-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="05f43-1941">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="05f43-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="05f43-1942">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="05f43-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="05f43-1943">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="05f43-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="05f43-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="05f43-1945">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="05f43-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="05f43-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="05f43-1946">Az.Automation</span></span>
* <span data-ttu-id="05f43-1947">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="05f43-1948">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="05f43-1949">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="05f43-1950">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="05f43-1951">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="05f43-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="05f43-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-1952">Az.Compute</span></span>
* <span data-ttu-id="05f43-1953">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="05f43-1954">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="05f43-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="05f43-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="05f43-1956">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="05f43-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="05f43-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="05f43-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="05f43-1958">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="05f43-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="05f43-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-1959">Az.Network</span></span>
* <span data-ttu-id="05f43-1960">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="05f43-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="05f43-1961">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="05f43-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="05f43-1962">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="05f43-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="05f43-1963">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="05f43-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="05f43-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="05f43-1965">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="05f43-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="05f43-1966">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="05f43-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="05f43-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="05f43-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="05f43-1968">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="05f43-1969">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="05f43-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="05f43-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="05f43-1970">Az.Relay</span></span>
* <span data-ttu-id="05f43-1971">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="05f43-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="05f43-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-1972">Az.Resources</span></span>
* <span data-ttu-id="05f43-1973">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="05f43-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="05f43-1974">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="05f43-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="05f43-1975">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="05f43-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="05f43-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-1977">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="05f43-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="05f43-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-1978">Az.Sql</span></span>
* <span data-ttu-id="05f43-1979">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="05f43-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="05f43-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="05f43-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="05f43-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="05f43-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="05f43-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="05f43-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="05f43-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="05f43-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="05f43-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="05f43-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="05f43-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="05f43-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="05f43-1988">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="05f43-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="05f43-1989">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="05f43-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="05f43-1990">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="05f43-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="05f43-1991">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="05f43-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="05f43-1992">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="05f43-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="05f43-1993">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="05f43-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="05f43-1994">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="05f43-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="05f43-1995">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="05f43-1996">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="05f43-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="05f43-1997">一般</span><span class="sxs-lookup"><span data-stu-id="05f43-1997">General</span></span>
* <span data-ttu-id="05f43-1998">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="05f43-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="05f43-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="05f43-1999">Az.Profile</span></span>
* <span data-ttu-id="05f43-2000">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="05f43-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="05f43-2001">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="05f43-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="05f43-2002">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="05f43-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="05f43-2003">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="05f43-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="05f43-2004">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="05f43-2005">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="05f43-2006">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-2008">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="05f43-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-2009">Az.Compute</span></span>
* <span data-ttu-id="05f43-2010">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="05f43-2011">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="05f43-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="05f43-2012">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-2014">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="05f43-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="05f43-2015">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="05f43-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="05f43-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="05f43-2016">Az.Insights</span></span>
* <span data-ttu-id="05f43-2017">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="05f43-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="05f43-2018">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="05f43-2019">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="05f43-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="05f43-2020">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="05f43-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-2021">Az.Network</span></span>
* <span data-ttu-id="05f43-2022">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="05f43-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="05f43-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="05f43-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="05f43-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="05f43-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="05f43-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="05f43-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="05f43-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="05f43-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="05f43-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="05f43-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="05f43-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="05f43-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="05f43-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="05f43-2030">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-2031">Az.Resources</span></span>
* <span data-ttu-id="05f43-2032">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="05f43-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="05f43-2033">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="05f43-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="05f43-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="05f43-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="05f43-2035">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="05f43-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="05f43-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="05f43-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="05f43-2037">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="05f43-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="05f43-2038">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="05f43-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="05f43-2039">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="05f43-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="05f43-2040">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="05f43-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="05f43-2041">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="05f43-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="05f43-2042">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="05f43-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="05f43-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="05f43-2043">Az.Profile</span></span>
* <span data-ttu-id="05f43-2044">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="05f43-2045">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="05f43-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-2046">Az.Compute</span></span>
* <span data-ttu-id="05f43-2047">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="05f43-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="05f43-2048">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="05f43-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="05f43-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="05f43-2050">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="05f43-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="05f43-2051">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="05f43-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="05f43-2052">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="05f43-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="05f43-2053">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="05f43-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="05f43-2054">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="05f43-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-2055">Az.Network</span></span>
* <span data-ttu-id="05f43-2056">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="05f43-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="05f43-2057">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f43-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-2058">Az.Resources</span></span>
* <span data-ttu-id="05f43-2059">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="05f43-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="05f43-2060">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="05f43-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="05f43-2061">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="05f43-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="05f43-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="05f43-2062">Azure.Storage</span></span>
* <span data-ttu-id="05f43-2063">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="05f43-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="05f43-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="05f43-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="05f43-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="05f43-2066">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="05f43-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="05f43-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="05f43-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="05f43-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="05f43-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="05f43-2069">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="05f43-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="05f43-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="05f43-2070">Az.Compute</span></span>
* <span data-ttu-id="05f43-2071">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="05f43-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="05f43-2072">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="05f43-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="05f43-2073">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="05f43-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="05f43-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="05f43-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="05f43-2075">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="05f43-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="05f43-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="05f43-2076">Az.Network</span></span>
* <span data-ttu-id="05f43-2077">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="05f43-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="05f43-2078">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-2078">new cmdlets added</span></span>
    - <span data-ttu-id="05f43-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="05f43-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="05f43-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="05f43-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="05f43-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="05f43-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="05f43-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="05f43-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="05f43-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="05f43-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="05f43-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="05f43-2085">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="05f43-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="05f43-2086">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="05f43-2087">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="05f43-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="05f43-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="05f43-2088">Az.RedisCache</span></span>
* <span data-ttu-id="05f43-2089">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="05f43-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="05f43-2090">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="05f43-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="05f43-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="05f43-2091">Az.Resources</span></span>
* <span data-ttu-id="05f43-2092">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="05f43-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="05f43-2093">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="05f43-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="05f43-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="05f43-2094">Az.Sql</span></span>
* <span data-ttu-id="05f43-2095">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="05f43-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="05f43-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="05f43-2096">Az.Websites</span></span>
* <span data-ttu-id="05f43-2097">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="05f43-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="05f43-2098">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="05f43-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="05f43-2099">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="05f43-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="05f43-2100">初始版本</span><span class="sxs-lookup"><span data-stu-id="05f43-2100">Initial Release</span></span>
