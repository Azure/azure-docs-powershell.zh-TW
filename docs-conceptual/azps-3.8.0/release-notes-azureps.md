---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740536"
---
## <a name="380---april-2020"></a><span data-ttu-id="46deb-103">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="46deb-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-104">Az.Accounts</span></span>
* <span data-ttu-id="46deb-105">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="46deb-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-106">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-107">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="46deb-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="46deb-108">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-109">Az.Cdn</span></span>
* <span data-ttu-id="46deb-110">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="46deb-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-112">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="46deb-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="46deb-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-113">Az.Compute</span></span>
* <span data-ttu-id="46deb-114">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="46deb-115">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="46deb-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-116">Az.IotHub</span></span>
* <span data-ttu-id="46deb-117">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="46deb-118">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="46deb-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="46deb-119">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="46deb-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="46deb-120">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="46deb-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="46deb-121">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="46deb-122">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="46deb-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="46deb-123">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="46deb-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="46deb-124">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="46deb-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="46deb-125">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-125">New cmdlets are:</span></span>
    - <span data-ttu-id="46deb-126">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46deb-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46deb-127">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46deb-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46deb-128">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46deb-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="46deb-129">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="46deb-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="46deb-130">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="46deb-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-131">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-132">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="46deb-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="46deb-133">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="46deb-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="46deb-134">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="46deb-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="46deb-135">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="46deb-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="46deb-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="46deb-136">Az.Maintenance</span></span>
* <span data-ttu-id="46deb-137">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-138">Az.Monitor</span></span>
* <span data-ttu-id="46deb-139">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="46deb-140">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46deb-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46deb-141">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46deb-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46deb-142">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46deb-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46deb-143">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="46deb-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="46deb-144">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46deb-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="46deb-145">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46deb-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="46deb-146">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="46deb-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-147">Az.Network</span></span>
* <span data-ttu-id="46deb-148">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="46deb-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="46deb-149">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46deb-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="46deb-150">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46deb-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="46deb-151">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="46deb-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="46deb-152">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="46deb-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="46deb-153">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="46deb-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="46deb-154">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="46deb-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="46deb-155">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="46deb-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="46deb-156">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="46deb-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="46deb-157">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="46deb-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="46deb-158">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="46deb-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="46deb-159">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="46deb-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="46deb-160">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="46deb-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="46deb-161">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="46deb-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="46deb-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="46deb-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-165">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="46deb-166">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="46deb-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-168">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-169">Az.Sql</span></span>
* <span data-ttu-id="46deb-170">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="46deb-171">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="46deb-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-172">Az.Storage</span></span>
* <span data-ttu-id="46deb-173">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="46deb-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="46deb-174">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="46deb-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="46deb-175">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46deb-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="46deb-176">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46deb-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="46deb-177">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="46deb-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="46deb-178">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46deb-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46deb-179">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46deb-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46deb-180">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="46deb-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="46deb-181">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46deb-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46deb-182">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="46deb-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="46deb-183">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46deb-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="46deb-184">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="46deb-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="46deb-185">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="46deb-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="46deb-186">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="46deb-187">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="46deb-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-188">Az.Accounts</span></span>
* <span data-ttu-id="46deb-189">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="46deb-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-190">Az.Compute</span></span>
* <span data-ttu-id="46deb-191">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="46deb-192">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="46deb-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="46deb-193">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="46deb-194">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="46deb-195">[#11354]</span><span class="sxs-lookup"><span data-stu-id="46deb-195">[#11354]</span></span>
* <span data-ttu-id="46deb-196">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="46deb-197">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="46deb-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46deb-198">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="46deb-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46deb-199">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="46deb-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="46deb-200">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="46deb-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="46deb-201">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="46deb-202">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="46deb-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="46deb-203">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="46deb-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="46deb-204">[#11257]</span><span class="sxs-lookup"><span data-stu-id="46deb-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-205">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-206">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="46deb-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="46deb-207">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="46deb-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-209">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="46deb-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="46deb-210">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="46deb-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-211">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-212">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="46deb-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-213">Az.IotHub</span></span>
* <span data-ttu-id="46deb-214">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="46deb-215">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="46deb-216">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="46deb-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="46deb-217">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="46deb-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-218">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-219">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="46deb-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-220">Az.Monitor</span></span>
* <span data-ttu-id="46deb-221">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="46deb-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-222">Az.Network</span></span>
* <span data-ttu-id="46deb-223">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="46deb-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="46deb-224">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="46deb-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46deb-225">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="46deb-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="46deb-226">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="46deb-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="46deb-227">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="46deb-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="46deb-228">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-230">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-232">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="46deb-233">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="46deb-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="46deb-234">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="46deb-235">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="46deb-236">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="46deb-237">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-238">Az.Resources</span></span>
* <span data-ttu-id="46deb-239">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="46deb-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="46deb-240">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="46deb-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="46deb-241">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="46deb-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="46deb-242">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="46deb-242">Added example.</span></span>
* <span data-ttu-id="46deb-243">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="46deb-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="46deb-244">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-245">Az.Sql</span></span>
* <span data-ttu-id="46deb-246">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="46deb-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="46deb-247">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="46deb-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="46deb-248">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="46deb-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="46deb-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="46deb-249">Az.Support</span></span>
* <span data-ttu-id="46deb-250">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-251">Az.Websites</span></span>
* <span data-ttu-id="46deb-252">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="46deb-253">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="46deb-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46deb-254">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="46deb-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46deb-255">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="46deb-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="46deb-256">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="46deb-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="46deb-257">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="46deb-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-258">Az.Accounts</span></span>
* <span data-ttu-id="46deb-259">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="46deb-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="46deb-260">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="46deb-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="46deb-261">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-262">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-263">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="46deb-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="46deb-264">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="46deb-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="46deb-265">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="46deb-266">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="46deb-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-268">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="46deb-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-269">Az.IotHub</span></span>
* <span data-ttu-id="46deb-270">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46deb-271">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="46deb-272">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-273">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-274">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-275">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="46deb-276">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="46deb-277">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="46deb-278">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46deb-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="46deb-279">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46deb-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="46deb-280">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46deb-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="46deb-281">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="46deb-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="46deb-282">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="46deb-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46deb-283">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="46deb-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="46deb-284">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="46deb-285">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="46deb-286">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="46deb-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="46deb-287">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="46deb-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="46deb-288">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-289">Az.Monitor</span></span>
* <span data-ttu-id="46deb-290">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="46deb-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-291">Az.Network</span></span>
* <span data-ttu-id="46deb-292">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="46deb-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="46deb-293">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="46deb-294">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="46deb-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="46deb-295">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="46deb-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-296">Az.Resources</span></span>
* <span data-ttu-id="46deb-297">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="46deb-298">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="46deb-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="46deb-299">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="46deb-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="46deb-300">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="46deb-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="46deb-301">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="46deb-302">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="46deb-303">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="46deb-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="46deb-304">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46deb-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="46deb-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46deb-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46deb-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46deb-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="46deb-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46deb-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="46deb-308">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="46deb-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="46deb-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="46deb-310">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="46deb-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-311">Az.Sql</span></span>
* <span data-ttu-id="46deb-312">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="46deb-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="46deb-313">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="46deb-314">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="46deb-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="46deb-315">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="46deb-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="46deb-316">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="46deb-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="46deb-317">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="46deb-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="46deb-318">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="46deb-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="46deb-319">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="46deb-320">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-321">Az.Storage</span></span>
* <span data-ttu-id="46deb-322">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="46deb-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="46deb-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="46deb-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="46deb-324">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="46deb-325">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="46deb-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="46deb-326">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="46deb-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-327">Az.Websites</span></span>
* <span data-ttu-id="46deb-328">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="46deb-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="46deb-329">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="46deb-330">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="46deb-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="46deb-331">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="46deb-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="46deb-332">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="46deb-333">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="46deb-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-334">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-334">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-335">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="46deb-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="46deb-336">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="46deb-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="46deb-337">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-338">Az.Accounts</span></span>
* <span data-ttu-id="46deb-339">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="46deb-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-340">Az.Automation</span></span>
* <span data-ttu-id="46deb-341">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-343">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="46deb-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="46deb-344">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-345">Az.Compute</span></span>
* <span data-ttu-id="46deb-346">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="46deb-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-347">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-348">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="46deb-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-349">Az.IotHub</span></span>
* <span data-ttu-id="46deb-350">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="46deb-351">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="46deb-352">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-353">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-354">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="46deb-355">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="46deb-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-356">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-357">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="46deb-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-358">Az.Monitor</span></span>
* <span data-ttu-id="46deb-359">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="46deb-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="46deb-360">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="46deb-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="46deb-361">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="46deb-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-362">Az.Network</span></span>
* <span data-ttu-id="46deb-363">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="46deb-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="46deb-364">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="46deb-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46deb-365">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="46deb-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="46deb-366">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="46deb-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="46deb-367">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-367">No new cmdlets are added.</span></span> <span data-ttu-id="46deb-368">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="46deb-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-370">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-371">Az.Resources</span></span>
* <span data-ttu-id="46deb-372">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="46deb-373">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="46deb-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="46deb-374">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="46deb-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="46deb-375">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="46deb-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="46deb-376">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="46deb-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="46deb-377">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="46deb-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="46deb-378">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="46deb-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="46deb-379">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="46deb-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-380">Az.Sql</span></span>
* <span data-ttu-id="46deb-381">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="46deb-382">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="46deb-383">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="46deb-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46deb-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46deb-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46deb-385">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46deb-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46deb-386">Az.StorageSync</span></span>
* <span data-ttu-id="46deb-387">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="46deb-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="46deb-388">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="46deb-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-389">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-389">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-390">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="46deb-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="46deb-391">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="46deb-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-392">Az.Accounts</span></span>
* <span data-ttu-id="46deb-393">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="46deb-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="46deb-394">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="46deb-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-395">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-396">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="46deb-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="46deb-397">**New-AzApiManagementProduct**\* 和 **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="46deb-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="46deb-398">https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="46deb-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="46deb-399">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="46deb-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-400">Az.Compute</span></span>
* <span data-ttu-id="46deb-401">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="46deb-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="46deb-402">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="46deb-403">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="46deb-404">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="46deb-405">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-406">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-407">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="46deb-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46deb-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46deb-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="46deb-409">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="46deb-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="46deb-410">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="46deb-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-411">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-412">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="46deb-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-413">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-414">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="46deb-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-415">Az.Network</span></span>
* <span data-ttu-id="46deb-416">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="46deb-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="46deb-417">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="46deb-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="46deb-418">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46deb-419">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="46deb-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="46deb-420">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="46deb-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="46deb-421">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="46deb-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="46deb-422">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="46deb-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="46deb-423">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="46deb-424">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-424">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="46deb-426">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="46deb-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46deb-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="46deb-428">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-430">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="46deb-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="46deb-431">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="46deb-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="46deb-432">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="46deb-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="46deb-433">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="46deb-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-435">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="46deb-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="46deb-436">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-437">Az.Resources</span></span>
* <span data-ttu-id="46deb-438">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="46deb-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="46deb-439">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-440">Az.Sql</span></span>
<span data-ttu-id="46deb-441">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="46deb-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-442">Az.Storage</span></span>
* <span data-ttu-id="46deb-443">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="46deb-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="46deb-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="46deb-445">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="46deb-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="46deb-446">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="46deb-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-447">Az.Websites</span></span>
* <span data-ttu-id="46deb-448">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="46deb-449">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="46deb-450">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="46deb-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-451">Az.Accounts</span></span>
* <span data-ttu-id="46deb-452">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-453">Az.Cdn</span></span>
* <span data-ttu-id="46deb-454">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="46deb-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-455">Az.Compute</span></span>
* <span data-ttu-id="46deb-456">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="46deb-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="46deb-458">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46deb-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46deb-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46deb-460">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="46deb-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46deb-461">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="46deb-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="46deb-462">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="46deb-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46deb-463">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="46deb-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="46deb-464">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="46deb-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46deb-465">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="46deb-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="46deb-466">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="46deb-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="46deb-467">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="46deb-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="46deb-468">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46deb-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46deb-469">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="46deb-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="46deb-470">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46deb-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46deb-471">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="46deb-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="46deb-472">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="46deb-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="46deb-473">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="46deb-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="46deb-474">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="46deb-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="46deb-475">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="46deb-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="46deb-476">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="46deb-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="46deb-477">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="46deb-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-478">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-479">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="46deb-480">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="46deb-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="46deb-481">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="46deb-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="46deb-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="46deb-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="46deb-483">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="46deb-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-484">Az.EventHub</span></span>
* <span data-ttu-id="46deb-485">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="46deb-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-486">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-487">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="46deb-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46deb-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46deb-488">Az.MachineLearning</span></span>
* <span data-ttu-id="46deb-489">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="46deb-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46deb-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="46deb-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="46deb-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="46deb-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46deb-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="46deb-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46deb-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="46deb-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="46deb-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="46deb-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="46deb-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="46deb-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="46deb-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-497">Az.Network</span></span>
* <span data-ttu-id="46deb-498">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="46deb-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-500">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="46deb-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="46deb-501">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="46deb-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46deb-502">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="46deb-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="46deb-503">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="46deb-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-504">Az.Resources</span></span>
* <span data-ttu-id="46deb-505">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="46deb-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-506">Az.Sql</span></span>
* <span data-ttu-id="46deb-507">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="46deb-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="46deb-508">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="46deb-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="46deb-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="46deb-510">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="46deb-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-511">Az.Storage</span></span>
* <span data-ttu-id="46deb-512">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="46deb-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="46deb-514">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="46deb-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="46deb-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="46deb-516">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="46deb-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="46deb-517">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-517">General</span></span>
* <span data-ttu-id="46deb-518">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="46deb-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-519">Az.Accounts</span></span>
* <span data-ttu-id="46deb-520">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="46deb-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="46deb-521">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46deb-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-522">Az.Batch</span></span>
* <span data-ttu-id="46deb-523">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="46deb-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-524">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-525">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="46deb-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-526">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-527">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="46deb-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="46deb-528">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="46deb-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46deb-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46deb-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="46deb-530">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="46deb-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-531">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-532">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="46deb-533">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="46deb-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="46deb-534">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-535">Az.Monitor</span></span>
* <span data-ttu-id="46deb-536">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="46deb-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="46deb-537">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="46deb-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="46deb-538">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="46deb-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-539">Az.Network</span></span>
* <span data-ttu-id="46deb-540">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="46deb-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-541">Az.Resources</span></span>
* <span data-ttu-id="46deb-542">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="46deb-543">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-544">Az.Sql</span></span>
* <span data-ttu-id="46deb-545">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="46deb-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-546">Az.Storage</span></span>
* <span data-ttu-id="46deb-547">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="46deb-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="46deb-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="46deb-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="46deb-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46deb-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="46deb-550">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="46deb-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="46deb-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="46deb-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="46deb-552">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="46deb-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="46deb-553">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="46deb-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="46deb-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="46deb-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="46deb-556">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="46deb-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="46deb-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="46deb-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="46deb-558">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="46deb-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="46deb-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="46deb-560">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="46deb-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-561">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-561">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-562">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="46deb-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="46deb-563">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="46deb-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-564">Az.Compute</span></span>
* <span data-ttu-id="46deb-565">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="46deb-565">VM Reapply feature</span></span>
    - <span data-ttu-id="46deb-566">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="46deb-567">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="46deb-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="46deb-568">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46deb-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="46deb-569">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="46deb-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="46deb-570">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="46deb-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46deb-571">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="46deb-572">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="46deb-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="46deb-573">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="46deb-574">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="46deb-575">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="46deb-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="46deb-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="46deb-577">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="46deb-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46deb-578">取得訂單</span><span class="sxs-lookup"><span data-stu-id="46deb-578">Get the Order</span></span>
* <span data-ttu-id="46deb-579">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="46deb-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46deb-580">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="46deb-580">Create new Order</span></span>
* <span data-ttu-id="46deb-581">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="46deb-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="46deb-582">移除訂單</span><span class="sxs-lookup"><span data-stu-id="46deb-582">Remove the Order</span></span>
* <span data-ttu-id="46deb-583">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="46deb-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="46deb-584">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="46deb-584">Now creates Local Share</span></span>
* <span data-ttu-id="46deb-585">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="46deb-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="46deb-586">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="46deb-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="46deb-587">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="46deb-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="46deb-588">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="46deb-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="46deb-589">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="46deb-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46deb-590">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="46deb-591">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="46deb-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46deb-592">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="46deb-592">Create new Triggers</span></span>
* <span data-ttu-id="46deb-593">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="46deb-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="46deb-594">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="46deb-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-595">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-596">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="46deb-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="46deb-597">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="46deb-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-599">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="46deb-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-600">Az.EventHub</span></span>
* <span data-ttu-id="46deb-601">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="46deb-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-602">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-603">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="46deb-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="46deb-604">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="46deb-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="46deb-605">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="46deb-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="46deb-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="46deb-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-607">Az.Network</span></span>
* <span data-ttu-id="46deb-608">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="46deb-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="46deb-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="46deb-609">Az.PrivateDns</span></span>
* <span data-ttu-id="46deb-610">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="46deb-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-612">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="46deb-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="46deb-613">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="46deb-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="46deb-614">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="46deb-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46deb-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46deb-615">Az.RedisCache</span></span>
* <span data-ttu-id="46deb-616">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="46deb-617">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="46deb-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="46deb-618">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="46deb-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-619">Az.Resources</span></span>
- <span data-ttu-id="46deb-620">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="46deb-621">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="46deb-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="46deb-622">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="46deb-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="46deb-623">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="46deb-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="46deb-624">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="46deb-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-625">Az.Sql</span></span>
* <span data-ttu-id="46deb-626">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="46deb-627">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46deb-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="46deb-628">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="46deb-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="46deb-629">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-629">General</span></span>
* <span data-ttu-id="46deb-630">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="46deb-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-631">Az.Accounts</span></span>
* <span data-ttu-id="46deb-632">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="46deb-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46deb-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46deb-633">Az.Advisor</span></span>
* <span data-ttu-id="46deb-634">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="46deb-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46deb-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-635">Az.Batch</span></span>
* <span data-ttu-id="46deb-636">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="46deb-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="46deb-637">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="46deb-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="46deb-638">這會影響 **Get-AzBatchAccount**。</span><span class="sxs-lookup"><span data-stu-id="46deb-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="46deb-639">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="46deb-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="46deb-640">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="46deb-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="46deb-641">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask**。</span><span class="sxs-lookup"><span data-stu-id="46deb-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="46deb-642">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="46deb-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="46deb-643">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="46deb-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="46deb-644">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="46deb-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="46deb-645">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46deb-646">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="46deb-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="46deb-647">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="46deb-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="46deb-648">將 **Get-AzBatchApplicationPackage**、**New-AzBatchApplicationPackage**、**Remove-AzBatchApplicationPackage**、**Get-AzBatchApplication**、**New-AzBatchApplication**、**Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="46deb-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="46deb-649">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="46deb-650">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="46deb-651">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="46deb-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="46deb-652">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="46deb-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="46deb-653">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="46deb-654">已移除 **AzBatchPoolOSVersion**。</span><span class="sxs-lookup"><span data-stu-id="46deb-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="46deb-655">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="46deb-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="46deb-656">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="46deb-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46deb-657">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="46deb-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="46deb-658">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="46deb-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="46deb-659">已移除 **AzBatchNodeAgentSku**，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="46deb-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="46deb-660">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="46deb-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="46deb-661">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="46deb-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="46deb-662">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46deb-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="46deb-663">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="46deb-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="46deb-664">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="46deb-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="46deb-665">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="46deb-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="46deb-666">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="46deb-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="46deb-667">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="46deb-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="46deb-668">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="46deb-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="46deb-669">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="46deb-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="46deb-670">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="46deb-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="46deb-671">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="46deb-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-672">Az.Cdn</span></span>
* <span data-ttu-id="46deb-673">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="46deb-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="46deb-674">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="46deb-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-675">Az.Compute</span></span>
* <span data-ttu-id="46deb-676">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="46deb-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="46deb-677">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="46deb-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="46deb-678">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46deb-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="46deb-679">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46deb-680">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="46deb-681">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="46deb-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="46deb-682">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="46deb-683">重大變更</span><span class="sxs-lookup"><span data-stu-id="46deb-683">Breaking changes</span></span>
    - <span data-ttu-id="46deb-684">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="46deb-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="46deb-685">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="46deb-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-686">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-687">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="46deb-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-689">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="46deb-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="46deb-690">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="46deb-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="46deb-691">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="46deb-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="46deb-692">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="46deb-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="46deb-693">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="46deb-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="46deb-694">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-695">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-696">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="46deb-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-697">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-698">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="46deb-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="46deb-699">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="46deb-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="46deb-700">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="46deb-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="46deb-701">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="46deb-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46deb-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46deb-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46deb-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46deb-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="46deb-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="46deb-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46deb-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="46deb-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46deb-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="46deb-707">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="46deb-708">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="46deb-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46deb-709">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="46deb-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="46deb-710">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="46deb-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="46deb-711">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="46deb-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="46deb-712">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="46deb-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="46deb-713">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="46deb-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="46deb-714">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="46deb-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="46deb-715">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="46deb-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="46deb-716">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="46deb-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="46deb-717">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="46deb-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="46deb-718">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="46deb-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="46deb-719">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="46deb-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-720">Az.IotHub</span></span>
* <span data-ttu-id="46deb-721">重大變更：</span><span class="sxs-lookup"><span data-stu-id="46deb-721">Breaking changes:</span></span>
    - <span data-ttu-id="46deb-722">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46deb-723">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="46deb-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46deb-724">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46deb-725">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="46deb-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46deb-726">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="46deb-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="46deb-727">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="46deb-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="46deb-728">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="46deb-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="46deb-729">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="46deb-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="46deb-730">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46deb-731">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="46deb-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="46deb-732">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="46deb-733">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="46deb-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-735">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="46deb-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-736">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="46deb-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="46deb-737">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="46deb-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="46deb-738">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="46deb-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-739">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="46deb-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-740">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="46deb-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-741">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="46deb-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-742">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-743">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="46deb-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-744">Az.Resources</span></span>
* <span data-ttu-id="46deb-745">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="46deb-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-746">Az.Network</span></span>
* <span data-ttu-id="46deb-747">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="46deb-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="46deb-748">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="46deb-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46deb-754">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="46deb-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="46deb-755">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-755">New cmdlet:</span></span>
        - <span data-ttu-id="46deb-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="46deb-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="46deb-757">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="46deb-758">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="46deb-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="46deb-759">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="46deb-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="46deb-760">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="46deb-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="46deb-761">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="46deb-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="46deb-762">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="46deb-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="46deb-763">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="46deb-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="46deb-764">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-764">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="46deb-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="46deb-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46deb-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46deb-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="46deb-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="46deb-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="46deb-770">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="46deb-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="46deb-771">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="46deb-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46deb-772">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="46deb-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46deb-773">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="46deb-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="46deb-774">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="46deb-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="46deb-775">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="46deb-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="46deb-776">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="46deb-777">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-777">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="46deb-779">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="46deb-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46deb-780">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46deb-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46deb-781">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46deb-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46deb-782">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46deb-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46deb-783">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46deb-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="46deb-784">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="46deb-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="46deb-785">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="46deb-786">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-786">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="46deb-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="46deb-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="46deb-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="46deb-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="46deb-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="46deb-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="46deb-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="46deb-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="46deb-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="46deb-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="46deb-793">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="46deb-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46deb-794">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="46deb-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="46deb-795">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="46deb-796">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="46deb-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="46deb-797">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="46deb-798">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="46deb-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="46deb-799">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="46deb-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="46deb-800">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="46deb-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="46deb-801">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="46deb-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="46deb-802">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="46deb-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="46deb-803">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="46deb-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="46deb-804">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-804">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="46deb-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="46deb-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="46deb-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-810">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="46deb-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-811">Az.Sql</span></span>
* <span data-ttu-id="46deb-812">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="46deb-813">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="46deb-814">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="46deb-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="46deb-815">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="46deb-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="46deb-816">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="46deb-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="46deb-817">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46deb-818">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="46deb-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="46deb-819">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="46deb-820">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="46deb-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-821">Az.Storage</span></span>
* <span data-ttu-id="46deb-822">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="46deb-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="46deb-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46deb-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46deb-825">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="46deb-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="46deb-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46deb-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="46deb-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46deb-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="46deb-828">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="46deb-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="46deb-829">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-829">General</span></span>
* <span data-ttu-id="46deb-830">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-831">Az.Accounts</span></span>
* <span data-ttu-id="46deb-832">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="46deb-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-833">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-834">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="46deb-835">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-836">Az.Automation</span></span>
* <span data-ttu-id="46deb-837">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46deb-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-838">Az.Batch</span></span>
* <span data-ttu-id="46deb-839">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="46deb-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-840">Az.Compute</span></span>
* <span data-ttu-id="46deb-841">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="46deb-842">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="46deb-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="46deb-843">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="46deb-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="46deb-844">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="46deb-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-845">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-846">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="46deb-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="46deb-847">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="46deb-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="46deb-848">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="46deb-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-850">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="46deb-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="46deb-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="46deb-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="46deb-852">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="46deb-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="46deb-853">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="46deb-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="46deb-854">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="46deb-855">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="46deb-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-856">Az.IotHub</span></span>
* <span data-ttu-id="46deb-857">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="46deb-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="46deb-858">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="46deb-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-859">Az.Monitor</span></span>
* <span data-ttu-id="46deb-860">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="46deb-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="46deb-861">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="46deb-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="46deb-862">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="46deb-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="46deb-863">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="46deb-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-864">Az.Network</span></span>
* <span data-ttu-id="46deb-865">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="46deb-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="46deb-866">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="46deb-867">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-867">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="46deb-869">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46deb-870">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="46deb-871">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="46deb-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46deb-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46deb-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46deb-875">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="46deb-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="46deb-876">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="46deb-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="46deb-877">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="46deb-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="46deb-878">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="46deb-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46deb-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46deb-879">Az.RedisCache</span></span>
* <span data-ttu-id="46deb-880">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="46deb-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-881">Az.Sql</span></span>
* <span data-ttu-id="46deb-882">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-883">Az.Storage</span></span>
* <span data-ttu-id="46deb-884">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="46deb-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="46deb-885">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="46deb-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46deb-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="46deb-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="46deb-887">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="46deb-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="46deb-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46deb-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46deb-889">Az.StorageSync</span></span>
* <span data-ttu-id="46deb-890">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="46deb-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-891">Az.Websites</span></span>
* <span data-ttu-id="46deb-892">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="46deb-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="46deb-893">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="46deb-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46deb-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-894">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-895">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="46deb-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="46deb-896">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="46deb-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="46deb-897">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="46deb-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-898">Az.Automation</span></span>
* <span data-ttu-id="46deb-899">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="46deb-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="46deb-900">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="46deb-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="46deb-901">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="46deb-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-902">Az.Compute</span></span>
* <span data-ttu-id="46deb-903">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="46deb-904">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="46deb-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46deb-905">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="46deb-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="46deb-906">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="46deb-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="46deb-907">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="46deb-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="46deb-908">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="46deb-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="46deb-909">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="46deb-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="46deb-910">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="46deb-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="46deb-911">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-912">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-913">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="46deb-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="46deb-914">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="46deb-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-915">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-916">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="46deb-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-917">Az.IotHub</span></span>
* <span data-ttu-id="46deb-918">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="46deb-919">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="46deb-920">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="46deb-920">New cmdlets are:</span></span>
    - <span data-ttu-id="46deb-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46deb-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46deb-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46deb-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46deb-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46deb-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="46deb-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="46deb-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-925">Az.Monitor</span></span>
* <span data-ttu-id="46deb-926">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="46deb-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="46deb-927">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="46deb-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="46deb-928">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="46deb-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="46deb-929">**ActionGroups** 要求的 api-version 現在為 **2019-06-01**，之前為 **2018-03-01**。</span><span class="sxs-lookup"><span data-stu-id="46deb-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="46deb-930">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="46deb-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="46deb-931">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="46deb-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="46deb-932">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="46deb-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="46deb-933">**注意**：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="46deb-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="46deb-934">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="46deb-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46deb-935">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="46deb-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="46deb-936">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="46deb-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="46deb-937">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="46deb-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="46deb-938">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="46deb-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="46deb-939">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="46deb-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="46deb-940">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="46deb-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="46deb-941">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="46deb-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="46deb-942">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="46deb-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="46deb-943">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="46deb-944">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="46deb-945">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="46deb-945">Overall improved help files</span></span>
* <span data-ttu-id="46deb-946">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-947">Az.Network</span></span>
* <span data-ttu-id="46deb-948">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="46deb-949">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="46deb-950">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="46deb-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="46deb-951">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="46deb-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="46deb-952">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="46deb-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="46deb-953">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="46deb-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="46deb-954">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="46deb-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="46deb-955">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="46deb-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="46deb-956">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="46deb-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="46deb-957">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="46deb-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="46deb-958">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="46deb-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="46deb-959">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="46deb-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="46deb-960">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-960">New cmdlets</span></span>
        - <span data-ttu-id="46deb-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="46deb-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="46deb-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="46deb-963">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="46deb-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46deb-964">New-VpnSite</span></span>
        - <span data-ttu-id="46deb-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="46deb-965">Update-VpnSite</span></span>
        - <span data-ttu-id="46deb-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-966">New-VpnConnection</span></span>
        - <span data-ttu-id="46deb-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-967">Update-VpnConnection</span></span>
* <span data-ttu-id="46deb-968">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-970">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="46deb-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="46deb-971">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="46deb-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-972">Az.Resources</span></span>
* <span data-ttu-id="46deb-973">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="46deb-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-975">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="46deb-976">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="46deb-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="46deb-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46deb-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46deb-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46deb-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46deb-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46deb-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46deb-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46deb-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="46deb-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46deb-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46deb-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46deb-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46deb-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46deb-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46deb-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46deb-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46deb-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="46deb-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="46deb-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="46deb-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="46deb-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="46deb-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="46deb-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="46deb-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="46deb-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="46deb-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="46deb-990">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="46deb-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46deb-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46deb-991">Az.SignalR</span></span>
* <span data-ttu-id="46deb-992">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-993">Az.Sql</span></span>
* <span data-ttu-id="46deb-994">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="46deb-995">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="46deb-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="46deb-996">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="46deb-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="46deb-997">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="46deb-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="46deb-998">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="46deb-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-999">Az.Storage</span></span>
* <span data-ttu-id="46deb-1000">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="46deb-1001">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="46deb-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="46deb-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="46deb-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="46deb-1004">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="46deb-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="46deb-1006">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="46deb-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="46deb-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46deb-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46deb-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="46deb-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="46deb-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1011">Az.Websites</span></span>
* <span data-ttu-id="46deb-1012">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="46deb-1013">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="46deb-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="46deb-1014">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="46deb-1015">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="46deb-1016">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-1016">General</span></span>
* <span data-ttu-id="46deb-1017">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1018">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1019">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="46deb-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="46deb-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46deb-1020">Az.Aks</span></span>
* <span data-ttu-id="46deb-1021">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="46deb-1022">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="46deb-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-1024">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="46deb-1025">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="46deb-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="46deb-1026">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="46deb-1027">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="46deb-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="46deb-1028">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="46deb-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46deb-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-1029">Az.Batch</span></span>
* <span data-ttu-id="46deb-1030">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="46deb-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-1031">Az.Cdn</span></span>
* <span data-ttu-id="46deb-1032">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1033">Az.Compute</span></span>
* <span data-ttu-id="46deb-1034">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="46deb-1035">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="46deb-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="46deb-1036">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="46deb-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="46deb-1037">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="46deb-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="46deb-1038">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="46deb-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="46deb-1039">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="46deb-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="46deb-1040">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="46deb-1041">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1042">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1043">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="46deb-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="46deb-1044">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="46deb-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="46deb-1045">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="46deb-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="46deb-1046">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="46deb-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1048">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="46deb-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1049">Az.EventHub</span></span>
* <span data-ttu-id="46deb-1050">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="46deb-1051">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="46deb-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="46deb-1052">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="46deb-1053">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="46deb-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="46deb-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46deb-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46deb-1055">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-1056">Az.Monitor</span></span>
* <span data-ttu-id="46deb-1057">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1058">Az.Network</span></span>
* <span data-ttu-id="46deb-1059">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="46deb-1060">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="46deb-1061">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="46deb-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="46deb-1062">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="46deb-1063">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="46deb-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="46deb-1064">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="46deb-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="46deb-1065">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1067">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="46deb-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="46deb-1068">新增了範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1068">Added example</span></span>
    - <span data-ttu-id="46deb-1069">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="46deb-1070">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="46deb-1071">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1073">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1074">Az.Resources</span></span>
* <span data-ttu-id="46deb-1075">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="46deb-1076">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="46deb-1077">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="46deb-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="46deb-1078">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-1080">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="46deb-1081">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="46deb-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="46deb-1082">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-1084">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="46deb-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="46deb-1085">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="46deb-1086">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="46deb-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="46deb-1087">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="46deb-1088">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="46deb-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="46deb-1089">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1090">Az.Sql</span></span>
* <span data-ttu-id="46deb-1091">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="46deb-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1092">Az.Storage</span></span>
* <span data-ttu-id="46deb-1093">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="46deb-1094">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="46deb-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="46deb-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="46deb-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46deb-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="46deb-1097">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="46deb-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="46deb-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46deb-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1099">Az.Websites</span></span>
* <span data-ttu-id="46deb-1100">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="46deb-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="46deb-1101">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1102">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1103">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="46deb-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="46deb-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="46deb-1105">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1106">Az.Automation</span></span>
* <span data-ttu-id="46deb-1107">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-1109">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1110">Az.Compute</span></span>
* <span data-ttu-id="46deb-1111">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46deb-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46deb-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46deb-1113">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="46deb-1114">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="46deb-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1115">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1116">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="46deb-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="46deb-1117">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1118">Az.EventHub</span></span>
* <span data-ttu-id="46deb-1119">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46deb-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46deb-1120">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-1121">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-1122">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46deb-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46deb-1123">Az.LogicApp</span></span>
* <span data-ttu-id="46deb-1124">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="46deb-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="46deb-1125">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="46deb-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="46deb-1127">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1128">Az.Network</span></span>
* <span data-ttu-id="46deb-1129">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="46deb-1130">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1130">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46deb-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46deb-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46deb-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="46deb-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="46deb-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="46deb-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="46deb-1139">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="46deb-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="46deb-1140">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="46deb-1141">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="46deb-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="46deb-1142">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="46deb-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="46deb-1143">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="46deb-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="46deb-1144">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="46deb-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="46deb-1145">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="46deb-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46deb-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="46deb-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="46deb-1149">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="46deb-1150">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="46deb-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="46deb-1151">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="46deb-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46deb-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="46deb-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="46deb-1155">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="46deb-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="46deb-1156">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="46deb-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="46deb-1157">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="46deb-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1159">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="46deb-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="46deb-1160">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="46deb-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1162">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46deb-1163">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="46deb-1164">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="46deb-1165">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="46deb-1166">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="46deb-1167">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46deb-1168">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="46deb-1169">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="46deb-1170">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="46deb-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="46deb-1171">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="46deb-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1172">Az.Resources</span></span>
- <span data-ttu-id="46deb-1173">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="46deb-1174">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="46deb-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-1176">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="46deb-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="46deb-1177">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1178">Az.Sql</span></span>
* <span data-ttu-id="46deb-1179">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="46deb-1180">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="46deb-1181">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="46deb-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1182">Az.Storage</span></span>
* <span data-ttu-id="46deb-1183">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46deb-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46deb-1184">Az.StorageSync</span></span>
* <span data-ttu-id="46deb-1185">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="46deb-1186">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="46deb-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1187">Az.Websites</span></span>
* <span data-ttu-id="46deb-1188">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="46deb-1189">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="46deb-1190">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="46deb-1191">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1192">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1193">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="46deb-1194">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="46deb-1195">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="46deb-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="46deb-1196">Az.Advisor</span></span>
* <span data-ttu-id="46deb-1197">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="46deb-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="46deb-1198">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="46deb-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="46deb-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-1200">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="46deb-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="46deb-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="46deb-1202">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="46deb-1203">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="46deb-1204">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="46deb-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46deb-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="46deb-1206">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1207">Az.Automation</span></span>
* <span data-ttu-id="46deb-1208">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="46deb-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1209">Az.Compute</span></span>
* <span data-ttu-id="46deb-1210">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1211">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1212">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="46deb-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46deb-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46deb-1213">Az.EventGrid</span></span>
* <span data-ttu-id="46deb-1214">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1215">Az.IotHub</span></span>
* <span data-ttu-id="46deb-1216">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1217">Az.Network</span></span>
* <span data-ttu-id="46deb-1218">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="46deb-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="46deb-1219">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-1221">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="46deb-1222">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="46deb-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1224">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="46deb-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1226">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="46deb-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1227">Az.Resources</span></span>
    - <span data-ttu-id="46deb-1228">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="46deb-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="46deb-1229">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="46deb-1230">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="46deb-1231">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="46deb-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-1233">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="46deb-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1234">Az.Sql</span></span>
* <span data-ttu-id="46deb-1235">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="46deb-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="46deb-1236">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="46deb-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="46deb-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46deb-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46deb-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="46deb-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46deb-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="46deb-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="46deb-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="46deb-1243">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="46deb-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1244">Az.Storage</span></span>
* <span data-ttu-id="46deb-1245">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="46deb-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="46deb-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46deb-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="46deb-1247">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="46deb-1248">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="46deb-1249">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="46deb-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="46deb-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="46deb-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="46deb-1252">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="46deb-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="46deb-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46deb-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="46deb-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="46deb-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="46deb-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="46deb-1255">Az.StorageSync</span></span>
* <span data-ttu-id="46deb-1256">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="46deb-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="46deb-1257">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1258">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1259">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="46deb-1260">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="46deb-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="46deb-1261">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="46deb-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="46deb-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="46deb-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="46deb-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1264">Az.Compute</span></span>
* <span data-ttu-id="46deb-1265">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="46deb-1266">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="46deb-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46deb-1267">Az.Dns</span></span>
* <span data-ttu-id="46deb-1268">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="46deb-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46deb-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46deb-1269">Az.EventGrid</span></span>
* <span data-ttu-id="46deb-1270">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="46deb-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="46deb-1271">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1271">New cmdlets:</span></span>
    - <span data-ttu-id="46deb-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46deb-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46deb-1273">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="46deb-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46deb-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46deb-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46deb-1275">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="46deb-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="46deb-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="46deb-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="46deb-1277">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="46deb-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46deb-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46deb-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46deb-1279">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="46deb-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="46deb-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="46deb-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="46deb-1281">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="46deb-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="46deb-1282">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="46deb-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46deb-1283">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="46deb-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="46deb-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="46deb-1285">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="46deb-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="46deb-1286">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="46deb-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="46deb-1287">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="46deb-1288">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="46deb-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="46deb-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="46deb-1290">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="46deb-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46deb-1291">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="46deb-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="46deb-1292">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="46deb-1293">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="46deb-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="46deb-1294">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="46deb-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="46deb-1295">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="46deb-1296">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="46deb-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="46deb-1297">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="46deb-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="46deb-1298">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="46deb-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="46deb-1299">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="46deb-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="46deb-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="46deb-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="46deb-1301">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="46deb-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="46deb-1302">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="46deb-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="46deb-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="46deb-1305">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="46deb-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="46deb-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="46deb-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="46deb-1307">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="46deb-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1308">Az.Network</span></span>
* <span data-ttu-id="46deb-1309">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="46deb-1310">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1310">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="46deb-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="46deb-1312">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="46deb-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="46deb-1313">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1313">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="46deb-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="46deb-1315">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="46deb-1316">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1316">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46deb-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46deb-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="46deb-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="46deb-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="46deb-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="46deb-1322">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46deb-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="46deb-1323">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1323">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46deb-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46deb-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46deb-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46deb-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="46deb-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="46deb-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="46deb-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="46deb-1328">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="46deb-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="46deb-1329">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="46deb-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="46deb-1330">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="46deb-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="46deb-1331">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="46deb-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="46deb-1332">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="46deb-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="46deb-1333">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="46deb-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="46deb-1334">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="46deb-1335">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="46deb-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="46deb-1336">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="46deb-1337">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="46deb-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="46deb-1338">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="46deb-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="46deb-1339">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="46deb-1340">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="46deb-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="46deb-1341">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="46deb-1342">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="46deb-1343">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="46deb-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="46deb-1344">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="46deb-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="46deb-1345">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="46deb-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="46deb-1346">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="46deb-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="46deb-1347">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="46deb-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="46deb-1348">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="46deb-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46deb-1349">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="46deb-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="46deb-1350">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="46deb-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1352">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="46deb-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1353">Az.Resources</span></span>
* <span data-ttu-id="46deb-1354">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="46deb-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="46deb-1355">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46deb-1356">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="46deb-1357">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="46deb-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-1359">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1360">Az.Sql</span></span>
* <span data-ttu-id="46deb-1361">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="46deb-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="46deb-1362">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="46deb-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="46deb-1363">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="46deb-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="46deb-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46deb-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46deb-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46deb-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46deb-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46deb-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="46deb-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46deb-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="46deb-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="46deb-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1369">Az.Storage</span></span>
* <span data-ttu-id="46deb-1370">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="46deb-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="46deb-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="46deb-1372">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="46deb-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1374">Az.Websites</span></span>
* <span data-ttu-id="46deb-1375">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="46deb-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="46deb-1376">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="46deb-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="46deb-1377">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="46deb-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-1378">Az.Cdn</span></span>
* <span data-ttu-id="46deb-1379">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="46deb-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1380">Az.Compute</span></span>
* <span data-ttu-id="46deb-1381">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="46deb-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="46deb-1382">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="46deb-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1383">Az.EventHub</span></span>
* <span data-ttu-id="46deb-1384">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="46deb-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="46deb-1385">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46deb-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1386">Az.Network</span></span>
* <span data-ttu-id="46deb-1387">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="46deb-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="46deb-1388">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="46deb-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-1390">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1392">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="46deb-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-1394">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46deb-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-1396">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="46deb-1397">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1398">Az.Sql</span></span>
* <span data-ttu-id="46deb-1399">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="46deb-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="46deb-1400">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="46deb-1401">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="46deb-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="46deb-1402">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1403">Az.Websites</span></span>
* <span data-ttu-id="46deb-1404">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="46deb-1405">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="46deb-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-1407">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="46deb-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="46deb-1408">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="46deb-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="46deb-1409">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="46deb-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="46deb-1410">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="46deb-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="46deb-1411">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="46deb-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="46deb-1412">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="46deb-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="46deb-1413">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="46deb-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="46deb-1414">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="46deb-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="46deb-1415">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="46deb-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="46deb-1416">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="46deb-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="46deb-1417">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="46deb-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="46deb-1418">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="46deb-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="46deb-1419">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="46deb-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="46deb-1420">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="46deb-1421">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="46deb-1422">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="46deb-1423">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="46deb-1424">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="46deb-1425">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="46deb-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="46deb-1426">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="46deb-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="46deb-1427">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="46deb-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="46deb-1428">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="46deb-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="46deb-1429">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="46deb-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="46deb-1430">已更新 Cmdlet **New-AzApiManagement**，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="46deb-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="46deb-1431">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="46deb-1432">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="46deb-1433">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="46deb-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="46deb-1434">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="46deb-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="46deb-1435">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="46deb-1436">已更新 Cmdlet **Get-AzApiManagementSsoToken**，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="46deb-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="46deb-1437">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="46deb-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="46deb-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="46deb-1439">已更新 Cmdlet **Export-AzApiManagementApi**，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="46deb-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="46deb-1440">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46deb-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46deb-1441">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="46deb-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="46deb-1442">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="46deb-1443">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="46deb-1444">已更新 Cmdlet **Get-AzApiManagementPolicy**，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="46deb-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="46deb-1445">已更新 Cmdlet **Set-AzApiManagementPolicy**，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="46deb-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="46deb-1446">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46deb-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46deb-1447">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="46deb-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46deb-1448">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="46deb-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="46deb-1449">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="46deb-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="46deb-1450">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="46deb-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="46deb-1451">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="46deb-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="46deb-1452">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="46deb-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="46deb-1453">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="46deb-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="46deb-1454">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="46deb-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="46deb-1455">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="46deb-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="46deb-1456">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="46deb-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="46deb-1457">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="46deb-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="46deb-1458">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="46deb-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="46deb-1459">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="46deb-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="46deb-1460">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="46deb-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="46deb-1461">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="46deb-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="46deb-1462">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="46deb-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="46deb-1463">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="46deb-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46deb-1464">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="46deb-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46deb-1465">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="46deb-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46deb-1466">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46deb-1467">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="46deb-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="46deb-1468">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="46deb-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="46deb-1469">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="46deb-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="46deb-1470">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="46deb-1471">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="46deb-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="46deb-1472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="46deb-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="46deb-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="46deb-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="46deb-1474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="46deb-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="46deb-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="46deb-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="46deb-1476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="46deb-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="46deb-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="46deb-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="46deb-1478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="46deb-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="46deb-1479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="46deb-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="46deb-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="46deb-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="46deb-1481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="46deb-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="46deb-1482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="46deb-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="46deb-1483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="46deb-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1484">Az.Automation</span></span>
* <span data-ttu-id="46deb-1485">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="46deb-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="46deb-1486">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="46deb-1487">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="46deb-1488">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="46deb-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="46deb-1489">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="46deb-1490">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="46deb-1491">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="46deb-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1492">Az.Compute</span></span>
* <span data-ttu-id="46deb-1493">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="46deb-1494">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="46deb-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1496">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="46deb-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-1497">Az.Monitor</span></span>
* <span data-ttu-id="46deb-1498">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1499">Az.Network</span></span>
* <span data-ttu-id="46deb-1500">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="46deb-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="46deb-1501">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="46deb-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="46deb-1503">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="46deb-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1504">Az.Resources</span></span>
* <span data-ttu-id="46deb-1505">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="46deb-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1506">Az.Sql</span></span>
* <span data-ttu-id="46deb-1507">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="46deb-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="46deb-1508">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1509">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1510">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-1512">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="46deb-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="46deb-1513">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="46deb-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1514">Az.Compute</span></span>
* <span data-ttu-id="46deb-1515">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="46deb-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="46deb-1516">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="46deb-1517">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="46deb-1518">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="46deb-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="46deb-1519">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="46deb-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="46deb-1520">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46deb-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="46deb-1521">重大變更</span><span class="sxs-lookup"><span data-stu-id="46deb-1521">Breaking changes</span></span>
    - <span data-ttu-id="46deb-1522">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="46deb-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="46deb-1523">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="46deb-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="46deb-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="46deb-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="46deb-1525">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="46deb-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="46deb-1526">Az.Dns</span></span>
* <span data-ttu-id="46deb-1527">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="46deb-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="46deb-1528">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="46deb-1529">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="46deb-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="46deb-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="46deb-1531">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="46deb-1532">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="46deb-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="46deb-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-1533">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-1534">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="46deb-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46deb-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="46deb-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46deb-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46deb-1537">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="46deb-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="46deb-1538">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="46deb-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="46deb-1539">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="46deb-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="46deb-1540">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="46deb-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-1541">Az.Monitor</span></span>
* <span data-ttu-id="46deb-1542">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="46deb-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="46deb-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="46deb-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="46deb-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="46deb-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="46deb-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="46deb-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="46deb-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="46deb-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="46deb-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="46deb-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="46deb-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="46deb-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="46deb-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46deb-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46deb-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46deb-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46deb-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="46deb-1554">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="46deb-1555">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1556">Az.Network</span></span>
* <span data-ttu-id="46deb-1557">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="46deb-1558">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1558">New cmdlets</span></span>
        - <span data-ttu-id="46deb-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46deb-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="46deb-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46deb-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="46deb-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46deb-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="46deb-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="46deb-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="46deb-1563">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="46deb-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46deb-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="46deb-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="46deb-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="46deb-1566">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="46deb-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="46deb-1567">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="46deb-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="46deb-1568">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="46deb-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-1570">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46deb-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="46deb-1571">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="46deb-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="46deb-1572">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="46deb-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1574">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="46deb-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="46deb-1575">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="46deb-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="46deb-1576">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="46deb-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="46deb-1577">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="46deb-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="46deb-1578">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="46deb-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="46deb-1579">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="46deb-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="46deb-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46deb-1580">Az.Relay</span></span>
* <span data-ttu-id="46deb-1581">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-1583">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1584">Az.Storage</span></span>
* <span data-ttu-id="46deb-1585">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="46deb-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="46deb-1586">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="46deb-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="46deb-1587">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="46deb-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="46deb-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="46deb-1589">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="46deb-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="46deb-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="46deb-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="46deb-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1593">Az.Websites</span></span>
* <span data-ttu-id="46deb-1594">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="46deb-1595">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="46deb-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="46deb-1596">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-1597">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-1598">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="46deb-1599">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46deb-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46deb-1600">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46deb-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46deb-1601">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46deb-1602">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="46deb-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46deb-1603">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46deb-1604">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1605">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1606">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="46deb-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="46deb-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-1607">Az.Batch</span></span>
* <span data-ttu-id="46deb-1608">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-1609">Az.Cdn</span></span>
* <span data-ttu-id="46deb-1610">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-1612">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1613">Az.Compute</span></span>
* <span data-ttu-id="46deb-1614">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="46deb-1615">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1616">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1617">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1618">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="46deb-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1620">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46deb-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46deb-1621">Az.EventGrid</span></span>
* <span data-ttu-id="46deb-1622">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1623">Az.EventHub</span></span>
* <span data-ttu-id="46deb-1624">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="46deb-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="46deb-1625">Az.HDInsight</span></span>
* <span data-ttu-id="46deb-1626">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1627">Az.IotHub</span></span>
* <span data-ttu-id="46deb-1628">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-1629">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-1630">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1631">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="46deb-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46deb-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="46deb-1633">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="46deb-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46deb-1634">Az.Media</span></span>
* <span data-ttu-id="46deb-1635">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-1636">Az.Monitor</span></span>
  * <span data-ttu-id="46deb-1637">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="46deb-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="46deb-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="46deb-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="46deb-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="46deb-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46deb-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46deb-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46deb-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="46deb-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="46deb-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="46deb-1643">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="46deb-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1644">Az.Network</span></span>
* <span data-ttu-id="46deb-1645">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1646">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="46deb-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="46deb-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="46deb-1648">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1650">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="46deb-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="46deb-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="46deb-1652">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1654">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1655">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="46deb-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="46deb-1656">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="46deb-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="46deb-1657">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="46deb-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46deb-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46deb-1658">Az.RedisCache</span></span>
* <span data-ttu-id="46deb-1659">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1660">Az.Resources</span></span>
* <span data-ttu-id="46deb-1661">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1662">Az.Sql</span></span>
* <span data-ttu-id="46deb-1663">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="46deb-1664">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1665">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="46deb-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="46deb-1666">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="46deb-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="46deb-1667">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="46deb-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="46deb-1668">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="46deb-1669">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="46deb-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1670">Az.Websites</span></span>
* <span data-ttu-id="46deb-1671">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="46deb-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="46deb-1672">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="46deb-1673">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="46deb-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="46deb-1674">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="46deb-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="46deb-1675">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-1676">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-1677">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="46deb-1678">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46deb-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46deb-1679">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46deb-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46deb-1680">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46deb-1681">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="46deb-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46deb-1682">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46deb-1683">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="46deb-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1684">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1685">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46deb-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="46deb-1687">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="46deb-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="46deb-1688">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="46deb-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1689">Az.Automation</span></span>
* <span data-ttu-id="46deb-1690">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="46deb-1691">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="46deb-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="46deb-1692">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="46deb-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1693">Az.Compute</span></span>
* <span data-ttu-id="46deb-1694">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="46deb-1695">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="46deb-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="46deb-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="46deb-1697">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="46deb-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1698">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1699">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="46deb-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="46deb-1700">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1701">Az.Resources</span></span>
* <span data-ttu-id="46deb-1702">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="46deb-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="46deb-1703">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="46deb-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="46deb-1704">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="46deb-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="46deb-1705">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46deb-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="46deb-1706">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="46deb-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="46deb-1707">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="46deb-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1708">Az.Sql</span></span>
* <span data-ttu-id="46deb-1709">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="46deb-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1710">Az.Storage</span></span>
* <span data-ttu-id="46deb-1711">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="46deb-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="46deb-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46deb-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="46deb-1713">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="46deb-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46deb-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46deb-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="46deb-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="46deb-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="46deb-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="46deb-1718">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="46deb-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46deb-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="46deb-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="46deb-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="46deb-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="46deb-1723">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="46deb-1724">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="46deb-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="46deb-1725">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="46deb-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="46deb-1726">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="46deb-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="46deb-1727">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="46deb-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="46deb-1728">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="46deb-1729">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="46deb-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46deb-1730">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="46deb-1731">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1732">Az.Automation</span></span>
* <span data-ttu-id="46deb-1733">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="46deb-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="46deb-1734">動態分組</span><span class="sxs-lookup"><span data-stu-id="46deb-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="46deb-1735">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="46deb-1735">Pre-Post script</span></span>
    * <span data-ttu-id="46deb-1736">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="46deb-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1737">Az.Compute</span></span>
* <span data-ttu-id="46deb-1738">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="46deb-1739">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="46deb-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-1740">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-1741">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1742">Az.Network</span></span>
* <span data-ttu-id="46deb-1743">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="46deb-1744">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="46deb-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1746">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="46deb-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="46deb-1747">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1748">Az.Resources</span></span>
* <span data-ttu-id="46deb-1749">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="46deb-1750">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="46deb-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1751">Az.Sql</span></span>
* <span data-ttu-id="46deb-1752">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="46deb-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1753">Az.Storage</span></span>
* <span data-ttu-id="46deb-1754">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="46deb-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="46deb-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46deb-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46deb-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="46deb-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="46deb-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="46deb-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="46deb-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="46deb-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="46deb-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1761">Az.Websites</span></span>
* <span data-ttu-id="46deb-1762">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="46deb-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="46deb-1763">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1764">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1765">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="46deb-1766">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1767">Az.Automation</span></span>
* <span data-ttu-id="46deb-1768">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="46deb-1769">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="46deb-1770">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="46deb-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-1771">Az.Cdn</span></span>
* <span data-ttu-id="46deb-1772">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1773">Az.Compute</span></span>
* <span data-ttu-id="46deb-1774">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1775">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1776">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="46deb-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46deb-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46deb-1777">Az.LogicApp</span></span>
* <span data-ttu-id="46deb-1778">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="46deb-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1779">Az.Network</span></span>
* <span data-ttu-id="46deb-1780">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1782">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="46deb-1783">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="46deb-1783">SDK Update</span></span>
* <span data-ttu-id="46deb-1784">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="46deb-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="46deb-1785">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="46deb-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1786">Az.Resources</span></span>
* <span data-ttu-id="46deb-1787">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="46deb-1788">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="46deb-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="46deb-1789">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="46deb-1790">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="46deb-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="46deb-1791">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="46deb-1792">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="46deb-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1793">Az.Sql</span></span>
* <span data-ttu-id="46deb-1794">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="46deb-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="46deb-1795">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="46deb-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1796">Az.Storage</span></span>
* <span data-ttu-id="46deb-1797">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46deb-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="46deb-1798">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="46deb-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="46deb-1800">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1801">Az.Automation</span></span>
* <span data-ttu-id="46deb-1802">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="46deb-1803">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="46deb-1804">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="46deb-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-1806">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="46deb-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1807">Az.Compute</span></span>
* <span data-ttu-id="46deb-1808">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="46deb-1809">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="46deb-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="46deb-1810">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="46deb-1811">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="46deb-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1813">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="46deb-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1814">Az.EventHub</span></span>
* <span data-ttu-id="46deb-1815">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="46deb-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-1816">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-1817">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="46deb-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46deb-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46deb-1818">Az.LogicApp</span></span>
* <span data-ttu-id="46deb-1819">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="46deb-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="46deb-1820">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="46deb-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="46deb-1821">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="46deb-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46deb-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46deb-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46deb-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46deb-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46deb-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="46deb-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="46deb-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="46deb-1826">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="46deb-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46deb-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46deb-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="46deb-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="46deb-1831">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="46deb-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="46deb-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-1832">Az.Monitor</span></span>
* <span data-ttu-id="46deb-1833">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1834">Az.Network</span></span>
* <span data-ttu-id="46deb-1835">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="46deb-1837">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="46deb-1838">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="46deb-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="46deb-1839">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="46deb-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1840">Az.Resources</span></span>
* <span data-ttu-id="46deb-1841">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46deb-1842">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="46deb-1843">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="46deb-1844">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1845">Az.Sql</span></span>
* <span data-ttu-id="46deb-1846">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="46deb-1847">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="46deb-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1848">Az.Websites</span></span>
* <span data-ttu-id="46deb-1849">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="46deb-1850">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1851">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1852">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="46deb-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46deb-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="46deb-1854">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="46deb-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1855">Az.Compute</span></span>
* <span data-ttu-id="46deb-1856">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="46deb-1857">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="46deb-1858">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="46deb-1860">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="46deb-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1861">Az.Resources</span></span>
* <span data-ttu-id="46deb-1862">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="46deb-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="46deb-1863">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="46deb-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="46deb-1864">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="46deb-1865">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="46deb-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1866">Az.Sql</span></span>
* <span data-ttu-id="46deb-1867">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="46deb-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="46deb-1868">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="46deb-1869">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="46deb-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="46deb-1870">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1871">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1872">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="46deb-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="46deb-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="46deb-1874">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="46deb-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="46deb-1876">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="46deb-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="46deb-1877">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1878">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1879">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="46deb-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="46deb-1880">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46deb-1881">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="46deb-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="46deb-1882">Az.Aks</span></span>
* <span data-ttu-id="46deb-1883">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="46deb-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-1884">Az.Automation</span></span>
* <span data-ttu-id="46deb-1885">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="46deb-1886">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="46deb-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="46deb-1887">Az.Cdn</span></span>
* <span data-ttu-id="46deb-1888">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1889">Az.Compute</span></span>
* <span data-ttu-id="46deb-1890">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="46deb-1891">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46deb-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="46deb-1892">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="46deb-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="46deb-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="46deb-1894">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="46deb-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="46deb-1895">Az.DataFactory</span></span>
* <span data-ttu-id="46deb-1896">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="46deb-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1898">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="46deb-1899">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="46deb-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="46deb-1900">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1901">Az.IotHub</span></span>
* <span data-ttu-id="46deb-1902">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="46deb-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-1903">Az.KeyVault</span></span>
* <span data-ttu-id="46deb-1904">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-1905">Az.Network</span></span>
* <span data-ttu-id="46deb-1906">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1907">Az.Resources</span></span>
* <span data-ttu-id="46deb-1908">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="46deb-1909">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="46deb-1910">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="46deb-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="46deb-1911">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="46deb-1912">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="46deb-1913">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="46deb-1914">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="46deb-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-1916">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="46deb-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="46deb-1917">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="46deb-1917">Fix some error messages.</span></span>
* <span data-ttu-id="46deb-1918">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="46deb-1919">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46deb-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46deb-1920">Az.SignalR</span></span>
* <span data-ttu-id="46deb-1921">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1922">Az.Sql</span></span>
* <span data-ttu-id="46deb-1923">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46deb-1924">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="46deb-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="46deb-1925">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="46deb-1926">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="46deb-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1927">Az.Storage</span></span>
* <span data-ttu-id="46deb-1928">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46deb-1929">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="46deb-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="46deb-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="46deb-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="46deb-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="46deb-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="46deb-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="46deb-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="46deb-1933">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1934">Az.Websites</span></span>
* <span data-ttu-id="46deb-1935">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="46deb-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="46deb-1936">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="46deb-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="46deb-1937">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="46deb-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="46deb-1938">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="46deb-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1939">Az.Accounts</span></span>
* <span data-ttu-id="46deb-1940">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="46deb-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-1941">Az.Compute</span></span>
* <span data-ttu-id="46deb-1942">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="46deb-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="46deb-1943">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="46deb-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="46deb-1944">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-1946">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="46deb-1947">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="46deb-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="46deb-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="46deb-1948">Az.EventGrid</span></span>
* <span data-ttu-id="46deb-1949">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="46deb-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="46deb-1950">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="46deb-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="46deb-1951">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="46deb-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46deb-1952">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="46deb-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46deb-1953">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="46deb-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46deb-1954">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="46deb-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="46deb-1955">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="46deb-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="46deb-1956">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="46deb-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="46deb-1957">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="46deb-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="46deb-1958">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="46deb-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="46deb-1959">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="46deb-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="46deb-1960">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="46deb-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="46deb-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="46deb-1961">Az.IotHub</span></span>
* <span data-ttu-id="46deb-1962">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="46deb-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="46deb-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="46deb-1963">Az.LogicApp</span></span>
* <span data-ttu-id="46deb-1964">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-1965">Az.Resources</span></span>
* <span data-ttu-id="46deb-1966">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="46deb-1967">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="46deb-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="46deb-1968">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="46deb-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46deb-1969">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="46deb-1970">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="46deb-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="46deb-1971">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="46deb-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="46deb-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="46deb-1972">Az.SignalR</span></span>
* <span data-ttu-id="46deb-1973">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-1974">Az.Sql</span></span>
* <span data-ttu-id="46deb-1975">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="46deb-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="46deb-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-1976">Az.Storage</span></span>
* <span data-ttu-id="46deb-1977">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="46deb-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46deb-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="46deb-1979">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="46deb-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="46deb-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="46deb-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-1981">Az.Websites</span></span>
* <span data-ttu-id="46deb-1982">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="46deb-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="46deb-1983">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="46deb-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="46deb-1984">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="46deb-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="46deb-1985">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-1985">General</span></span>

- <span data-ttu-id="46deb-1986">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="46deb-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="46deb-1987">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="46deb-1987">Online help for each module</span></span>
- <span data-ttu-id="46deb-1988">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="46deb-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="46deb-1989">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="46deb-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-1990">Az.Accounts</span></span>
- <span data-ttu-id="46deb-1991">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="46deb-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="46deb-1992">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="46deb-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46deb-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="46deb-1994">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="46deb-1994">Fixes for #7002</span></span>
- <span data-ttu-id="46deb-1995">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="46deb-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="46deb-1996">Az.Batch</span></span>
- <span data-ttu-id="46deb-1997">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="46deb-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="46deb-1998">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="46deb-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="46deb-1999">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="46deb-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="46deb-2000">Az.Billing</span></span>
- <span data-ttu-id="46deb-2001">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="46deb-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="46deb-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="46deb-2003">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="46deb-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="46deb-2004">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="46deb-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46deb-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="46deb-2006">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="46deb-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="46deb-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="46deb-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="46deb-2008">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46deb-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="46deb-2010">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="46deb-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="46deb-2011">Az.Monitor</span></span>
- <span data-ttu-id="46deb-2012">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="46deb-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="46deb-2013">Az.KeyVault</span></span>
- <span data-ttu-id="46deb-2014">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="46deb-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="46deb-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="46deb-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="46deb-2016">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="46deb-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="46deb-2017">Az.Media</span></span>
- <span data-ttu-id="46deb-2018">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="46deb-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46deb-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-2019">Az.Network</span></span>
<span data-ttu-id="46deb-2020">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="46deb-2021">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="46deb-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="46deb-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="46deb-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="46deb-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="46deb-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="46deb-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="46deb-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="46deb-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="46deb-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="46deb-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="46deb-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46deb-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46deb-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="46deb-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="46deb-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="46deb-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="46deb-2036">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="46deb-2037">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="46deb-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46deb-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46deb-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46deb-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="46deb-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="46deb-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="46deb-2041">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="46deb-2042">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="46deb-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="46deb-2044">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="46deb-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46deb-2045">Az.Profile</span></span>
- <span data-ttu-id="46deb-2046">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="46deb-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="46deb-2048">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="46deb-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2049">Az.Resources</span></span>
- <span data-ttu-id="46deb-2050">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46deb-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="46deb-2052">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="46deb-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="46deb-2053">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="46deb-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="46deb-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="46deb-2055">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="46deb-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="46deb-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-2056">Az.Sql</span></span>
- <span data-ttu-id="46deb-2057">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="46deb-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="46deb-2058">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="46deb-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="46deb-2059">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="46deb-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-2060">Az.Storage</span></span>
- <span data-ttu-id="46deb-2061">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46deb-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-2062">Az.Websites</span></span>
- <span data-ttu-id="46deb-2063">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="46deb-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="46deb-2064">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="46deb-2065">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-2065">General</span></span>

* <span data-ttu-id="46deb-2066">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="46deb-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="46deb-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-2067">Az.Compute</span></span>

* <span data-ttu-id="46deb-2068">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="46deb-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="46deb-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="46deb-2070">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="46deb-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="46deb-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="46deb-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="46deb-2072">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="46deb-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="46deb-2073">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="46deb-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="46deb-2074">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="46deb-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="46deb-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="46deb-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="46deb-2076">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="46deb-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="46deb-2077">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="46deb-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="46deb-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2078">Az.Resources</span></span>

* <span data-ttu-id="46deb-2079">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="46deb-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="46deb-2080">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="46deb-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="46deb-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-2081">Az.Sql</span></span>

* <span data-ttu-id="46deb-2082">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="46deb-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="46deb-2083">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="46deb-2084">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="46deb-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="46deb-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-2085">Az.Storage</span></span>

* <span data-ttu-id="46deb-2086">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="46deb-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="46deb-2087">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="46deb-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="46deb-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46deb-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46deb-2089">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="46deb-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="46deb-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46deb-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="46deb-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="46deb-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="46deb-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-2092">Az.Websites</span></span>

* <span data-ttu-id="46deb-2093">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="46deb-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="46deb-2094">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="46deb-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="46deb-2095">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="46deb-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="46deb-2096">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="46deb-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="46deb-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="46deb-2098">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="46deb-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="46deb-2099">Az.Automation</span></span>
* <span data-ttu-id="46deb-2100">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="46deb-2101">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="46deb-2102">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="46deb-2103">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="46deb-2104">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="46deb-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="46deb-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-2105">Az.Compute</span></span>
* <span data-ttu-id="46deb-2106">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="46deb-2107">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="46deb-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="46deb-2109">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="46deb-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="46deb-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="46deb-2111">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="46deb-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="46deb-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-2112">Az.Network</span></span>
* <span data-ttu-id="46deb-2113">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="46deb-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="46deb-2114">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="46deb-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="46deb-2115">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="46deb-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="46deb-2116">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="46deb-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="46deb-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="46deb-2118">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="46deb-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="46deb-2119">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="46deb-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="46deb-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="46deb-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="46deb-2121">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="46deb-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="46deb-2122">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="46deb-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="46deb-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="46deb-2123">Az.Relay</span></span>
* <span data-ttu-id="46deb-2124">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="46deb-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="46deb-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2125">Az.Resources</span></span>
* <span data-ttu-id="46deb-2126">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="46deb-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="46deb-2127">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="46deb-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="46deb-2128">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="46deb-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="46deb-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-2130">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="46deb-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="46deb-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-2131">Az.Sql</span></span>
* <span data-ttu-id="46deb-2132">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="46deb-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46deb-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46deb-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46deb-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="46deb-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="46deb-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46deb-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46deb-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46deb-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46deb-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46deb-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="46deb-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="46deb-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="46deb-2141">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="46deb-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="46deb-2142">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="46deb-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="46deb-2143">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="46deb-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="46deb-2144">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="46deb-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46deb-2145">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="46deb-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="46deb-2146">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="46deb-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="46deb-2147">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="46deb-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="46deb-2148">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="46deb-2149">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="46deb-2150">一般</span><span class="sxs-lookup"><span data-stu-id="46deb-2150">General</span></span>
* <span data-ttu-id="46deb-2151">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="46deb-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="46deb-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46deb-2152">Az.Profile</span></span>
* <span data-ttu-id="46deb-2153">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="46deb-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="46deb-2154">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="46deb-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="46deb-2155">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="46deb-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="46deb-2156">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="46deb-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="46deb-2157">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="46deb-2158">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="46deb-2159">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-2161">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="46deb-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-2162">Az.Compute</span></span>
* <span data-ttu-id="46deb-2163">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="46deb-2164">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="46deb-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="46deb-2165">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-2167">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="46deb-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="46deb-2168">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="46deb-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="46deb-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="46deb-2169">Az.Insights</span></span>
* <span data-ttu-id="46deb-2170">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="46deb-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="46deb-2171">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="46deb-2172">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="46deb-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="46deb-2173">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="46deb-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-2174">Az.Network</span></span>
* <span data-ttu-id="46deb-2175">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="46deb-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="46deb-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="46deb-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="46deb-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="46deb-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46deb-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="46deb-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="46deb-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="46deb-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="46deb-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="46deb-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="46deb-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="46deb-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="46deb-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="46deb-2183">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2184">Az.Resources</span></span>
* <span data-ttu-id="46deb-2185">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="46deb-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="46deb-2186">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="46deb-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="46deb-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="46deb-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="46deb-2188">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="46deb-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="46deb-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="46deb-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="46deb-2190">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="46deb-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="46deb-2191">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="46deb-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="46deb-2192">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="46deb-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="46deb-2193">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="46deb-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="46deb-2194">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="46deb-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="46deb-2195">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="46deb-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="46deb-2196">Az.Profile</span></span>
* <span data-ttu-id="46deb-2197">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="46deb-2198">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="46deb-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-2199">Az.Compute</span></span>
* <span data-ttu-id="46deb-2200">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="46deb-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="46deb-2201">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="46deb-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="46deb-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="46deb-2203">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="46deb-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="46deb-2204">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="46deb-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="46deb-2205">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="46deb-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46deb-2206">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="46deb-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="46deb-2207">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="46deb-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-2208">Az.Network</span></span>
* <span data-ttu-id="46deb-2209">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="46deb-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="46deb-2210">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46deb-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2211">Az.Resources</span></span>
* <span data-ttu-id="46deb-2212">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="46deb-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="46deb-2213">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="46deb-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="46deb-2214">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="46deb-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="46deb-2215">Azure.Storage</span></span>
* <span data-ttu-id="46deb-2216">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="46deb-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="46deb-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="46deb-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="46deb-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="46deb-2219">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="46deb-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="46deb-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="46deb-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="46deb-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="46deb-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="46deb-2222">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="46deb-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="46deb-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="46deb-2223">Az.Compute</span></span>
* <span data-ttu-id="46deb-2224">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="46deb-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="46deb-2225">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="46deb-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="46deb-2226">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="46deb-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="46deb-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="46deb-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="46deb-2228">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="46deb-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="46deb-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="46deb-2229">Az.Network</span></span>
* <span data-ttu-id="46deb-2230">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="46deb-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="46deb-2231">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2231">new cmdlets added</span></span>
    - <span data-ttu-id="46deb-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46deb-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="46deb-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46deb-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="46deb-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46deb-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="46deb-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="46deb-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="46deb-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="46deb-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="46deb-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="46deb-2238">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="46deb-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="46deb-2239">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="46deb-2240">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="46deb-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="46deb-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="46deb-2241">Az.RedisCache</span></span>
* <span data-ttu-id="46deb-2242">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="46deb-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="46deb-2243">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="46deb-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="46deb-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="46deb-2244">Az.Resources</span></span>
* <span data-ttu-id="46deb-2245">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="46deb-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="46deb-2246">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="46deb-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="46deb-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="46deb-2247">Az.Sql</span></span>
* <span data-ttu-id="46deb-2248">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="46deb-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="46deb-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="46deb-2249">Az.Websites</span></span>
* <span data-ttu-id="46deb-2250">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="46deb-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="46deb-2251">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="46deb-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="46deb-2252">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="46deb-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="46deb-2253">初始版本</span><span class="sxs-lookup"><span data-stu-id="46deb-2253">Initial Release</span></span>
