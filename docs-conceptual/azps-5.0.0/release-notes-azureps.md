---
title: Azure PowerShell 版本資訊
description: 了解 Azure PowerShell 模組的最新更新資訊。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4ab5639cfb997c5f9ee1286e6eacb97ef775239a
ms.sourcegitcommit: 63181e0af0e4468b0530fdb0495ed4d44bdfd1c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/31/2020
ms.locfileid: "93134857"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="6543a-103">Azure PowerShell 版本資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-103">Azure PowerShell release notes</span></span>

## <a name="500---october-2020"></a><span data-ttu-id="6543a-104">5.0.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6543a-104">5.0.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-105">Az.Accounts</span></span>
* <span data-ttu-id="6543a-106">[中斷性變更] 已移除 'Get-AzProfile' 和 'Select-AzProfile'</span><span class="sxs-lookup"><span data-stu-id="6543a-106">[Breaking Change] Removed 'Get-AzProfile' and 'Select-AzProfile'</span></span>
* <span data-ttu-id="6543a-107">已將 Azure Directory 驗證程式庫取代為 Microsoft Authentication Library (MSAL)</span><span class="sxs-lookup"><span data-stu-id="6543a-107">Replaced Azure Directory Authentication Library with Microsoft Authentication Library(MSAL)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-108">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-108">Az.Aks</span></span>
* <span data-ttu-id="6543a-109">[中斷性變更]已移除 'New-AzAksCluster' 和 'Set-AzAksCluster' 中的參數別名 'ClientIdAndSecret'。</span><span class="sxs-lookup"><span data-stu-id="6543a-109">[Breaking Change] Removed parameter alias 'ClientIdAndSecret' in 'New-AzAksCluster' and 'Set-AzAksCluster'.</span></span>
* <span data-ttu-id="6543a-110">[中斷性變更] 已將 'New-AzAksCluster' 中 'NodeVmSetType' 的預設值從 'AvailabilitySet' 變更為 'VirtualMachineScaleSets。</span><span class="sxs-lookup"><span data-stu-id="6543a-110">[Breaking Change] Changed the default value of 'NodeVmSetType' in 'New-AzAksCluster' from 'AvailabilitySet' to 'VirtualMachineScaleSets'.</span></span>
* <span data-ttu-id="6543a-111">[中斷性變更] 已將 'New-AzAksCluster' 中 'NetworkPlugin' 的預設值從 'None' 變更為 'azure'。</span><span class="sxs-lookup"><span data-stu-id="6543a-111">[Breaking Change] Changed the default value of 'NetworkPlugin' in 'New-AzAksCluster' from 'None' to 'azure'.</span></span>
* <span data-ttu-id="6543a-112">[中斷性變更] 已移除 'New-AzAksCluster' 中的參數 'NodeOsType'，因為其僅支援一個值 Linux。</span><span class="sxs-lookup"><span data-stu-id="6543a-112">[Breaking Change] Removed parameter 'NodeOsType' in 'New-AzAksCluster' as it supports only one value Linux.</span></span>

#### <a name="azbilling"></a><span data-ttu-id="6543a-113">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6543a-113">Az.Billing</span></span>
* <span data-ttu-id="6543a-114">已新增 'Get-AzBillingAccount' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-114">Added 'Get-AzBillingAccount' cmdlet</span></span>
* <span data-ttu-id="6543a-115">已新增 'Get-AzBillingProfile' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-115">Added 'Get-AzBillingProfile' cmdlet</span></span>
* <span data-ttu-id="6543a-116">已新增 'Get-AzInvoiceSection' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-116">Added 'Get-AzInvoiceSection' cmdlet</span></span>
* <span data-ttu-id="6543a-117">已在 'Get-AzBillingInvoice' Cmdlet 中新增參數</span><span class="sxs-lookup"><span data-stu-id="6543a-117">Added new parameters in 'Get-AzBillingInvoice' cmdlet</span></span>
* <span data-ttu-id="6543a-118">已從 Get-AzBillingInvoice Cmdlet 的回應中移除屬性 DownloadUrlExpiry、Type、BillingPeriodNames</span><span class="sxs-lookup"><span data-stu-id="6543a-118">Removed properties DownloadUrlExpiry, Type, BillingPeriodNames from the response of Get-AzBillingInvoice cmdlet</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-119">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-119">Az.Cdn</span></span>
* <span data-ttu-id="6543a-120">已新增 Cmdlet 來支援多個來源和私人連結功能</span><span class="sxs-lookup"><span data-stu-id="6543a-120">Added cmdlets to support multi-origin and private link functionality</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-121">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-121">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-122">已將 SDK 更新為 7.4.0-preview。</span><span class="sxs-lookup"><span data-stu-id="6543a-122">Updated SDK to 7.4.0-preview.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-123">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-123">Az.Compute</span></span>
* <span data-ttu-id="6543a-124">已將 '-VmssId' 參數新增至 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="6543a-124">Added '-VmssId' parameter to 'New-AzVm'</span></span>
* <span data-ttu-id="6543a-125">已將 'PlatformFaultDomainCount' 參數新增至 'New-AzVmss' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-125">Added 'PlatformFaultDomainCount' parameter to the 'New-AzVmss' cmdlet.</span></span>
* <span data-ttu-id="6543a-126">新的 Cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span><span class="sxs-lookup"><span data-stu-id="6543a-126">New cmdlet 'Get-AzDiskEncryptionSetAssociatedResource'</span></span>
* <span data-ttu-id="6543a-127">已將 'Tier' 和 'LogicalSectorSize' 選擇性參數新增至 New-AzDiskConfig Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-127">Added 'Tier' and 'LogicalSectorSize' optional parameters to the New-AzDiskConfig cmdlet.</span></span> 
* <span data-ttu-id="6543a-128">已將 'Tier'、'MaxSharesCount'、'DiskIOPSReadOnly' 和 'DiskMBpsReadOnly' 選擇性參數新增至 'New-AzDiskUpdateConfig' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-128">Added 'Tier', 'MaxSharesCount', 'DiskIOPSReadOnly', and 'DiskMBpsReadOnly' optional parameters to the 'New-AzDiskUpdateConfig' cmdlet.</span></span> 

#### <a name="azcontainerregistry"></a><span data-ttu-id="6543a-129">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6543a-129">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6543a-130">[重大變更] 將 API 版本更新為 2019-05-01</span><span class="sxs-lookup"><span data-stu-id="6543a-130">[Breaking Change] Updates API version to 2019-05-01</span></span>
* <span data-ttu-id="6543a-131">[中斷性變更] 已從 'New-AzContainerRegistry' 中移除 SKU 'Classic' 和參數 'StorageAccountName'</span><span class="sxs-lookup"><span data-stu-id="6543a-131">[Breaking Change] Removed SKU 'Classic' and parameter 'StorageAccountName' from 'New-AzContainerRegistry'</span></span>
* <span data-ttu-id="6543a-132">已新增 Cmdlet：'Connect-AzContainerRegistry'、'Import-AzContainerRegistry'、'Get-AzContainerRegistryUsage'、'New-AzContainerRegistryNetworkRule'、'Set-AzContainerRegistryNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="6543a-132">Added New cmdlets: 'Connect-AzContainerRegistry', 'Import-AzContainerRegistry', 'Get-AzContainerRegistryUsage', 'New-AzContainerRegistryNetworkRule', 'Set-AzContainerRegistryNetworkRule'</span></span>
* <span data-ttu-id="6543a-133">已將新參數 'NetworkRuleSet' 新增至 'Update-AzContainerRegistry'</span><span class="sxs-lookup"><span data-stu-id="6543a-133">Added new parameter 'NetworkRuleSet' to 'Update-AzContainerRegistry'</span></span>

#### <a name="azdatabricks"></a><span data-ttu-id="6543a-134">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="6543a-134">Az.Databricks</span></span>
* <span data-ttu-id="6543a-135">已修正可能導致更新 Databricks 工作區，但 `-EncryptionKeyVersion` 不會失敗的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-135">Fixed a bug that may cause updating databricks workspace without `-EncryptionKeyVersion` to fail.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-136">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-136">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-137">已將 ADF .Net SDK 版本更新為 4.12.0</span><span class="sxs-lookup"><span data-stu-id="6543a-137">Updated ADF .Net SDK version to 4.12.0</span></span>
* <span data-ttu-id="6543a-138">已將 ADF 加密用戶端 SDK 版本更新為 4.14.7587.7</span><span class="sxs-lookup"><span data-stu-id="6543a-138">Updated ADF encryption client SDK version to 4.14.7587.7</span></span>
* <span data-ttu-id="6543a-139">已新增 'Stop-AzDataFactoryV2TriggerRun' 和 'Invoke-AzDataFactoryV2TriggerRun' 命令</span><span class="sxs-lookup"><span data-stu-id="6543a-139">Added 'Stop-AzDataFactoryV2TriggerRun' and 'Invoke-AzDataFactoryV2TriggerRun' commands</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="6543a-140">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="6543a-140">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="6543a-141">需要 Location 屬性，才能建立最上層 arm 物件。</span><span class="sxs-lookup"><span data-stu-id="6543a-141">Require Location property for creating top level arm objects.</span></span>
        <span data-ttu-id="6543a-142">\* 使 `ApplicationGroupType` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="6543a-142">\* Made `ApplicationGroupType` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="6543a-143">\* 使 `HostPoolArmPath` 成為 `New-AzWvdApplicationGroup` 的必要項。</span><span class="sxs-lookup"><span data-stu-id="6543a-143">\* Made `HostPoolArmPath` required for `New-AzWvdApplicationGroup`.</span></span>
        <span data-ttu-id="6543a-144">\* 已新增 `New-AzWvdHostPool`的 `PreferredAppGroupType`。</span><span class="sxs-lookup"><span data-stu-id="6543a-144">\* Added `PreferredAppGroupType` for `New-AzWvdHostPool`.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6543a-145">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6543a-145">Az.Functions</span></span>
* <span data-ttu-id="6543a-146">[中斷性變更] 已從 'Get-AzFunctionApp' 的所有參數集 (一個參數集除外) 中移除 'IncludeSlot' 切換參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-146">[Breaking Change] Removed 'IncludeSlot' switch parameter from all but one parameter set of 'Get-AzFunctionApp'.</span></span> <span data-ttu-id="6543a-147">若已指定 '-IncludeSlot'，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="6543a-147">The cmdlet now supports retrieving deployment slots in the results when '-IncludeSlot' is specified.</span></span> 
* <span data-ttu-id="6543a-148">已更新 'New-AzFunctionApp'：</span><span class="sxs-lookup"><span data-stu-id="6543a-148">Updated 'New-AzFunctionApp':</span></span>
  - <span data-ttu-id="6543a-149">已修正 - DisableApplicationInsights，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="6543a-149">Fixed -DisableApplicationInsights so that no application insights project is created when this option is specified.</span></span> <span data-ttu-id="6543a-150">[#12728]</span><span class="sxs-lookup"><span data-stu-id="6543a-150">[#12728]</span></span>
  - <span data-ttu-id="6543a-151">[中斷性變更] 已移除建立 PowerShell 6.2 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-151">[Breaking Change] Removed support to create PowerShell 6.2 function apps.</span></span>
  - <span data-ttu-id="6543a-152">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="6543a-152">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="6543a-153">[中斷性變更] 若未指定 RuntimeVersion 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="6543a-153">[Breaking Change] Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the RuntimeVersion parameter is not specified.</span></span>
  - <span data-ttu-id="6543a-154">[中斷性變更] 若未指定 RuntimeVersion 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="6543a-154">[Breaking Change] Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the RuntimeVersion parameter is not specified.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-155">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-155">Az.HDInsight</span></span>
 * <span data-ttu-id="6543a-156">針對 New-AzHDInsightCluster Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-156">For New-AzHDInsightCluster cmdlet:</span></span>
     - <span data-ttu-id="6543a-157">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="6543a-157">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="6543a-158">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6543a-158">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="6543a-159">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="6543a-159">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="6543a-160">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="6543a-160">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6543a-161">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="6543a-161">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6543a-162">已新增參數：'StorageFileSystem' 和 'StorageAccountManagedIdentity' 來支援 ADLSGen2</span><span class="sxs-lookup"><span data-stu-id="6543a-162">Added new parameters: 'StorageFileSystem' and 'StorageAccountManagedIdentity' to support ADLSGen2</span></span>
     - <span data-ttu-id="6543a-163">已新增參數 'EnableIDBroker' 來支援 HDInsight 識別碼代理程式</span><span class="sxs-lookup"><span data-stu-id="6543a-163">Added new parameter 'EnableIDBroker' to Support HDInsight ID Broker</span></span>
     - <span data-ttu-id="6543a-164">已新增參數：'KafkaClientGroupId'、'KafkaClientGroupName' 和 'KafkaManagementNodeSize' 來支援 Kafka Rest Proxy</span><span class="sxs-lookup"><span data-stu-id="6543a-164">Added new parameters: 'KafkaClientGroupId', 'KafkaClientGroupName' and 'KafkaManagementNodeSize' to support Kafka Rest Proxy</span></span>
 * <span data-ttu-id="6543a-165">針對 New-AzHDInsightClusterConfig Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-165">For New-AzHDInsightClusterConfig cmdlet:</span></span>
     - <span data-ttu-id="6543a-166">已將參數 'DefaultStorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="6543a-166">Replaced parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
     - <span data-ttu-id="6543a-167">已將參數 'DefaultStorageAccountKey' 取代為 'StorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6543a-167">Replaced parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
     - <span data-ttu-id="6543a-168">已將參數 'DefaultStorageAccountType' 取代為 'StorageAccountType'</span><span class="sxs-lookup"><span data-stu-id="6543a-168">Replaced parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
     - <span data-ttu-id="6543a-169">已移除參數 'PublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="6543a-169">Removed parameter 'PublicNetworkAccessType'</span></span>
     - <span data-ttu-id="6543a-170">已移除參數 'OutboundPublicNetworkAccessType'</span><span class="sxs-lookup"><span data-stu-id="6543a-170">Removed parameter 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="6543a-171">針對 AzHDInsightDefaultStorage Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-171">For Set-AzHDInsightDefaultStorage cmdlet:</span></span>
    - <span data-ttu-id="6543a-172">已將參數 'StorageAccountName' 取代為 'StorageAccountResourceId'</span><span class="sxs-lookup"><span data-stu-id="6543a-172">Replaced parameter 'StorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="6543a-173">針對 AzHDInsightSecurityProfile Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-173">For Add-AzHDInsightSecurityProfile cmdlet:</span></span>
    - <span data-ttu-id="6543a-174">已將參數 'Domain' 取代為 'DomainResourceId'</span><span class="sxs-lookup"><span data-stu-id="6543a-174">Replaced parameter 'Domain' with 'DomainResourceId'</span></span>
    - <span data-ttu-id="6543a-175">已移除參數 'OrganizationalUnitDN' 的強制需求</span><span class="sxs-lookup"><span data-stu-id="6543a-175">Removed the mandatory requirement for parameter 'OrganizationalUnitDN'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-176">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-176">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-177">[中斷性變更] 已淘汰 'New-AzKeyVault' 中的參數 DisableSoftDelete 和 'Update-AzKeyVault' 中的 EnableSoftDelete 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-177">[Breaking Change] Deprecated parameter DisableSoftDelete in 'New-AzKeyVault' and EnableSoftDelete in 'Update-AzKeyVault'</span></span>
* <span data-ttu-id="6543a-178">[中斷性變更] 已移除屬性 SecretValueText 來避免直接顯示 SecretValue [#12266]</span><span class="sxs-lookup"><span data-stu-id="6543a-178">[Breaking Change] Removed attribute SecretValueText to avoid displaying SecretValue directly [#12266]</span></span>
* <span data-ttu-id="6543a-179">支援的新資源類型：受控 HSM</span><span class="sxs-lookup"><span data-stu-id="6543a-179">Supported new resource type: managed HSM</span></span>
    - <span data-ttu-id="6543a-180">受控 HSM 的 CRUD 和要在受控 HSM 上操作金鑰的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-180">CRUD of managed HSM and cmdlets to operate keys on managed HSM</span></span>
    - <span data-ttu-id="6543a-181">完整 HSM 備份/還原、AES 金鑰建立、安全性網域備份/還原、RBAC</span><span class="sxs-lookup"><span data-stu-id="6543a-181">Full HSM backup/restore, AES key creation, security domain backup/restore, RBAC</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6543a-182">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6543a-182">Az.ManagedServices</span></span>
* <span data-ttu-id="6543a-183">[中斷性變更] 已更新參數命名慣例和相關範例</span><span class="sxs-lookup"><span data-stu-id="6543a-183">[Breaking Change] Updated parameters naming conventions and associated examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-184">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-184">Az.Network</span></span>
* <span data-ttu-id="6543a-185">[中斷性變更] 已移除參數 'HostedSubnet' 並改為新增 'Subnet'</span><span class="sxs-lookup"><span data-stu-id="6543a-185">[Breaking Change] Removed parameter 'HostedSubnet' and added 'Subnet' instead</span></span>
* <span data-ttu-id="6543a-186">已針對虛擬路由器對等路由新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-186">Added new cmdlets for Virtual Router Peer Routes</span></span>
    - <span data-ttu-id="6543a-187">'Get-AzVirtualRouterPeerLearnedRoute'</span><span class="sxs-lookup"><span data-stu-id="6543a-187">'Get-AzVirtualRouterPeerLearnedRoute'</span></span>
    - <span data-ttu-id="6543a-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span><span class="sxs-lookup"><span data-stu-id="6543a-188">'Get-AzVirtualRouterPeerAdvertisedRoute'</span></span>
* <span data-ttu-id="6543a-189">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-189">Updated New-AzFirewall cmdlet:</span></span>
    - <span data-ttu-id="6543a-190">已新增參數 '-SkuTier'</span><span class="sxs-lookup"><span data-stu-id="6543a-190">Added parameter '-SkuTier'</span></span>
    - <span data-ttu-id="6543a-191">已新增參數 '-SkuName' 並將 Sku 設為此項的別名</span><span class="sxs-lookup"><span data-stu-id="6543a-191">Added parameter '-SkuName' and made Sku as Alias for this</span></span>
    - <span data-ttu-id="6543a-192">已移除參數 '-Sku'</span><span class="sxs-lookup"><span data-stu-id="6543a-192">Removed parameter '-Sku'</span></span>
* <span data-ttu-id="6543a-193">[中斷性變更] 讓 'Connectionlink' 成為 'Start-AzVpnConnectionPacketCapture' 和 'Stop-AzVpnConnectionPacketCapture' 中的必要引數</span><span class="sxs-lookup"><span data-stu-id="6543a-193">[Breaking Change] Made 'Connectionlink' argument mandatory in 'Start-AzVpnConnectionPacketCapture' and 'Stop-AzVpnConnectionPacketCapture'</span></span>
* <span data-ttu-id="6543a-194">[中斷性變更] 已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' 來移除參數 '-Filter'</span><span class="sxs-lookup"><span data-stu-id="6543a-194">[Breaking Change] Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' to remove parameter '-Filter'</span></span>
* <span data-ttu-id="6543a-195">[中斷性變更] 已將 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' Cmdlet 取代為 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span><span class="sxs-lookup"><span data-stu-id="6543a-195">[Breaking Change] Replaced 'New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject' cmdlet with 'New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject'</span></span>
* <span data-ttu-id="6543a-196">已更新 'New-AzNetworkWatcherConnectionMonitorEndPointObject' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-196">Updated 'New-AzNetworkWatcherConnectionMonitorEndPointObject' cmdlet:</span></span>
    - <span data-ttu-id="6543a-197">已新增參數 '-Type'</span><span class="sxs-lookup"><span data-stu-id="6543a-197">Added parameter '-Type'</span></span>
    - <span data-ttu-id="6543a-198">已新增參數 '-CoverageLevel'</span><span class="sxs-lookup"><span data-stu-id="6543a-198">Added parameter '-CoverageLevel'</span></span>
    - <span data-ttu-id="6543a-199">已新增參數 '-Scope'</span><span class="sxs-lookup"><span data-stu-id="6543a-199">Added parameter '-Scope'</span></span>
* <span data-ttu-id="6543a-200">已使用新參數 '-DestinationPortBehavior' 更新 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-200">Updated 'New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject' cmdlet with new parameter '-DestinationPortBehavior'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-201">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-201">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-202">已修正參與者權限的工作負載還原。</span><span class="sxs-lookup"><span data-stu-id="6543a-202">Fixing Workload Restore for contributor permissions.</span></span>
* <span data-ttu-id="6543a-203">已針對 Restore-AzRecoveryServicesBackupItem Cmdlet 新增參數集和驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-203">Added new parameter sets and validations for Restore-AzRecoveryServicesBackupItem cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-204">Az.Resources</span></span>
* <span data-ttu-id="6543a-205">已修正剖析錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-205">Fixed parsing bug</span></span>
* <span data-ttu-id="6543a-206">已更新 ARM 範本 What-If Cmdlet 以便從結果中移除預覽訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-206">Updated ARM template What-If cmdlets to remove preview message from results</span></span>
* <span data-ttu-id="6543a-207">已修正 '-WhatIf ' 設定於較高範圍時範本部署 Cmdlet 損毀的問題 [#13038]</span><span class="sxs-lookup"><span data-stu-id="6543a-207">Fixed an issue where template deployment cmdlets crash if '-WhatIf' is set at a higher scope [#13038]</span></span>
* <span data-ttu-id="6543a-208">已修正範本部署 Cmdlet 未保留範本參數大小寫的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-208">Fixed an issue where template deployment cmdlets does not preserve case for template parameters</span></span>
* <span data-ttu-id="6543a-209">已新增要在 'Export-AzResourceGroup' Cmdlet 中使用的預設 API 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-209">Added a default API version to be used in 'Export-AzResourceGroup' cmdlet</span></span>
* <span data-ttu-id="6543a-210">已針對範本規格 ('Get-AzTemplateSpec'、'Set-AzTemplateSpec'、'New-AzTemplateSpec'、'Remove-AzTemplateSpec'、'Export-AzTemplateSpec') 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-210">Added cmdlets for Template Specs ('Get-AzTemplateSpec', 'Set-AzTemplateSpec', 'New-AzTemplateSpec', 'Remove-AzTemplateSpec', 'Export-AzTemplateSpec')</span></span>
* <span data-ttu-id="6543a-211">已新增使用現有的部署 Cmdlet 來部署範本規格的支援 (透過新的 -TemplateSpecId 參數)</span><span class="sxs-lookup"><span data-stu-id="6543a-211">Added support for deploying Template Specs using existing deployment cmdlets (via the new -TemplateSpecId parameter)</span></span> 
* <span data-ttu-id="6543a-212">已將 'Get-AzResourceGroupDeploymentOperation' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-212">Updated 'Get-AzResourceGroupDeploymentOperation' to use the SDK.</span></span>
* <span data-ttu-id="6543a-213">已從 '\*-AzDeployment' Cmdlet 中移除 '-ApiVersion' 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-213">Removed '-ApiVersion' parameter from '\*-AzDeployment' cmdlets.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-214">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-214">Az.Sql</span></span>
* <span data-ttu-id="6543a-215">已將 DiffBackupIntervalInHours 新增至 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-215">Added DiffBackupIntervalInHours to 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span> 
* <span data-ttu-id="6543a-216">已修正未指定 networkIsolation 時 New-AzSqlDatabaseExport 失敗的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="6543a-216">Fixed issue where New-AzSqlDatabaseExport fails if networkIsolation not specified [#13097]</span></span>
* <span data-ttu-id="6543a-217">已修正 New-AzSqlDatabaseExport 和 New-AzSqlDatabaseImport 未在結果物件中傳回 OperationStatusLink 的問題 [#13097]</span><span class="sxs-lookup"><span data-stu-id="6543a-217">Fixed issue where New-AzSqlDatabaseExport and New-AzSqlDatabaseImport were not returning OperationStatusLink in the result object [#13097]</span></span>
* <span data-ttu-id="6543a-218">在備份儲存體備援警告中更新 Azure 配對區域 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-218">Update Azure Paired Regions URL in Backup Storage Redundancy Warnings</span></span> 

#### <a name="azstorage"></a><span data-ttu-id="6543a-219">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-219">Az.Storage</span></span>
* <span data-ttu-id="6543a-220">已移除淘汰的屬性 RestorePolicy.LastEnabledTime</span><span class="sxs-lookup"><span data-stu-id="6543a-220">Removed obsolete property RestorePolicy.LastEnabledTime</span></span>
    - <span data-ttu-id="6543a-221">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-221">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-222">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-222">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-223">'Get-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-223">'Get-AzStorageBlobServiceProperty'</span></span>
    - <span data-ttu-id="6543a-224">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-224">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6543a-225">將 DaysAfterModificationGreaterThan 的類型從 int 變更為 int？</span><span class="sxs-lookup"><span data-stu-id="6543a-225">Change Type of DaysAfterModificationGreaterThan from int to int?</span></span>
    - <span data-ttu-id="6543a-226">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-226">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6543a-227">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-227">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6543a-228">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="6543a-228">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="6543a-229">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6543a-229">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="6543a-230">使用存取層支援的建立/更新檔案共用</span><span class="sxs-lookup"><span data-stu-id="6543a-230">Supported create/update file share with access tier</span></span>
    - <span data-ttu-id="6543a-231">'New-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-231">'New-AzRmStorageShare'</span></span>
    - <span data-ttu-id="6543a-232">'Update-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-232">'Update-AzRmStorageShare'</span></span>
* <span data-ttu-id="6543a-233">在 Datalake Gen2 項目上以遞迴方式支援的設定/更新/移除 Acl</span><span class="sxs-lookup"><span data-stu-id="6543a-233">Supported set/update/remove Acl recursively on Datalake Gen2 item</span></span> 
    -  <span data-ttu-id="6543a-234">'Set-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6543a-234">'Set-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="6543a-235">'Update-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6543a-235">'Update-AzDataLakeGen2AclRecursive'</span></span> 
    -  <span data-ttu-id="6543a-236">'Remove-AzDataLakeGen2AclRecursive'</span><span class="sxs-lookup"><span data-stu-id="6543a-236">'Remove-AzDataLakeGen2AclRecursive'</span></span>
* <span data-ttu-id="6543a-237">具有新權限 x,t 支援的容器存取原則</span><span class="sxs-lookup"><span data-stu-id="6543a-237">Supported Container access policy with new permission x,t</span></span>
    -  <span data-ttu-id="6543a-238">'New-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-238">'New-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="6543a-239">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-239">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="6543a-240">已變更取得/設定容器存取原則 Cmdlet 的輸出，方法是將子屬性權限類型從 enum 變更為 String</span><span class="sxs-lookup"><span data-stu-id="6543a-240">Changed the output of get/set Container access policy cmdlet, by change the child property Permission type from enum to String</span></span>
    -  <span data-ttu-id="6543a-241">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-241">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    -  <span data-ttu-id="6543a-242">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-242">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
* <span data-ttu-id="6543a-243">已修正使用 json 設定管理原則的範例指令碼問題</span><span class="sxs-lookup"><span data-stu-id="6543a-243">Fixed a sample script issue of set management policy with json</span></span>
    -  <span data-ttu-id="6543a-244">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-244">'Set-AzStorageAccountManagementPolicy'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-245">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-245">Az.Websites</span></span>
* <span data-ttu-id="6543a-246">已新增 Premium V3 定價層的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-246">Added support for Premium V3 pricing tier</span></span>
* <span data-ttu-id="6543a-247">已將 WebSites SDK 更新為 3.1.0</span><span class="sxs-lookup"><span data-stu-id="6543a-247">Updated the WebSites SDK to 3.1.0</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="6543a-248">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="6543a-248">Thanks to our community contributors</span></span>
* <span data-ttu-id="6543a-249">@atul-ram，更新 Get-AzDelegation.md (#13176)</span><span class="sxs-lookup"><span data-stu-id="6543a-249">@atul-ram, Update Get-AzDelegation.md (#13176)</span></span>
* <span data-ttu-id="6543a-250">@dineshreddy007，在使用 WAC 權杖進行堆疊 HCI 註冊的情況下，取得正確指派的應用程式角色。</span><span class="sxs-lookup"><span data-stu-id="6543a-250">@dineshreddy007, Get the App Roles assigned correctly in case of Stack HCI registration using WAC token.</span></span> <span data-ttu-id="6543a-251">(#13249)</span><span class="sxs-lookup"><span data-stu-id="6543a-251">(#13249)</span></span>
* <span data-ttu-id="6543a-252">@kongou-ae，更新 New-AzOffice365PolicyProperty.md (#13217)</span><span class="sxs-lookup"><span data-stu-id="6543a-252">@kongou-ae, Update New-AzOffice365PolicyProperty.md (#13217)</span></span>
* <span data-ttu-id="6543a-253">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Set-AzApplicationGateway.md (#13150)</span><span class="sxs-lookup"><span data-stu-id="6543a-253">Lohith Chowdary Chilukuri (@Lochiluk), Update Set-AzApplicationGateway.md (#13150)</span></span>
* <span data-ttu-id="6543a-254">Matthew Burleigh (@mburleigh)</span><span class="sxs-lookup"><span data-stu-id="6543a-254">Matthew Burleigh (@mburleigh)</span></span>
  * <span data-ttu-id="6543a-255">將連結新增至文件 (#13203) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-255">Add links to PowerShell cmdlets referenced in the document (#13203)</span></span>
  * <span data-ttu-id="6543a-256">將連結新增至文件 (#13190) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-256">Add links to PowerShell cmdlets referenced in the document (#13190)</span></span>
  * <span data-ttu-id="6543a-257">將連結新增至文件 (#13189) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-257">Add links to PowerShell cmdlets referenced in the document (#13189)</span></span>
  * <span data-ttu-id="6543a-258">將連結新增至參考的 Cmdlet (#13137)</span><span class="sxs-lookup"><span data-stu-id="6543a-258">add links to referenced cmdlets (#13137)</span></span>
  * <span data-ttu-id="6543a-259">將連結新增至文件 (#13204) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-259">Add links to PowerShell cmdlets referenced in the document (#13204)</span></span>
  * <span data-ttu-id="6543a-260">將連結新增至文件 (#13205) 中參考的 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-260">Add links to PowerShell cmdlets referenced in the document (#13205)</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="6543a-261">4.8.0 - 2020 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6543a-261">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-262">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-262">Az.Accounts</span></span>
* <span data-ttu-id="6543a-263">已修正通用程式庫中的日期時間剖析問題 [#13045]</span><span class="sxs-lookup"><span data-stu-id="6543a-263">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-264">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-264">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-265">已新增 'New-AzCognitiveServicesAccountApiProperty' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-265">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="6543a-266">針對 'New-AzCognitiveServicesAccount' 和 'Set-AzCognitiveServicesAccount' 支援 'ApiProperty' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-266">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-267">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-267">Az.Compute</span></span>
* <span data-ttu-id="6543a-268">已藉由田 FailoverTypes 修正 'Update-ASRRecoveryPlan' 中的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-268">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="6543a-269">已將 '-Top' 和 '-OrderBy' 選擇性參數新增至 'Get-AzVmImage' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-269">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="6543a-270">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="6543a-270">Az.Databricks</span></span>
* <span data-ttu-id="6543a-271">'Az.Databricks' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="6543a-271">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="6543a-272">已新增虛擬網路對等互連的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-272">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-273">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-273">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-274">已修正輸出訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-274">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-275">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-275">Az.EventHub</span></span>
* <span data-ttu-id="6543a-276">已將選擇性切換參數 'TrustedServiceAccessEnabled' 新增至 'Set-AzEventHubNetworkRuleSet' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-276">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-277">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-277">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-278">已新增計劃的警告訊息，以取代 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-278">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="6543a-279">已新增計劃的警告訊息，以使用 'StorageAccountResourceId' 取代 'DefaultStorageAccountName' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-279">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="6543a-280">已新增計劃的警告訊息，以使用 'StorageAccountKey' 取代 'DefaultStorageAccountKey' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-280">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="6543a-281">已新增計劃的警告訊息，以使用 'StorageAccountType' 取代 'DefaultStorageAccountType' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-281">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="6543a-282">已新增計劃的警告訊息，以使用 'StorageContainer' 取代 'DefaultStorageContainer' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-282">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="6543a-283">已新增計劃的警告訊息，以使用 'StorageRootPath' 取代 'DefaultStorageRootPath' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-283">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-284">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-284">Az.IotHub</span></span>
* <span data-ttu-id="6543a-285">已更新裝置 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-285">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-286">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-286">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-287">已提供移除屬性 SecretValueText 的詳細日期</span><span class="sxs-lookup"><span data-stu-id="6543a-287">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6543a-288">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6543a-288">Az.ManagedServices</span></span>
* <span data-ttu-id="6543a-289">已在受控服務指派和定義的 Cmdlet 上更新中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="6543a-289">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-290">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-290">Az.Monitor</span></span>
* <span data-ttu-id="6543a-291">已修正無法隱藏警告訊息的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-291">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="6543a-292">[#12889]</span><span class="sxs-lookup"><span data-stu-id="6543a-292">[#12889]</span></span>
* <span data-ttu-id="6543a-293">在警示規則準則中支援 'SkipMetricValidation' 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-293">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="6543a-294">藉由導致略過計量驗證，允許針對尚未發出的自訂計量建立警示規則。</span><span class="sxs-lookup"><span data-stu-id="6543a-294">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-295">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-295">Az.Network</span></span>
* <span data-ttu-id="6543a-296">已將 Office365 原則新增至 VPNSite 資源</span><span class="sxs-lookup"><span data-stu-id="6543a-296">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="6543a-297">'New-AzO365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-297">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-298">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-298">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-299">已新增工作負載備份的容器名稱驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-299">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6543a-300">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6543a-300">Az.RedisCache</span></span>
* <span data-ttu-id="6543a-301">讓 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 不會因為註冊 Microsoft.Cache RP 相關的權限問題而失敗</span><span class="sxs-lookup"><span data-stu-id="6543a-301">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-302">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-302">Az.Sql</span></span>
* <span data-ttu-id="6543a-303">已將 BackupStorageRedundancy 新增至下列項目：</span><span class="sxs-lookup"><span data-stu-id="6543a-303">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="6543a-304">'Restore-AzureRmSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="6543a-304">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="6543a-305">'New-AzSqlDatabaseCopy'</span><span class="sxs-lookup"><span data-stu-id="6543a-305">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="6543a-306">'New-AzSqlDatabaseSecondary'</span><span class="sxs-lookup"><span data-stu-id="6543a-306">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="6543a-307">已針對所有 SQL DB 參考移除 BackupStorageRedundancy 參數的區分大小寫</span><span class="sxs-lookup"><span data-stu-id="6543a-307">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="6543a-308">已更新 BackupStorageRedundancy 警告訊息名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-308">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-309">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-309">Az.Storage</span></span>
* <span data-ttu-id="6543a-310">儲存體帳戶檔案服務上支援的啟用/停用/取得共用虛刪除屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-310">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="6543a-311">'Update-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-311">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="6543a-312">'Get-AzStorageFileServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-312">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="6543a-313">支援的清單檔案共用包含已刪除的儲存體帳戶，以及取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="6543a-313">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="6543a-314">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-314">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="6543a-315">支援還原已刪除檔案共用</span><span class="sxs-lookup"><span data-stu-id="6543a-315">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="6543a-316">'Restore-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-316">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="6543a-317">已變更修改 Blob 服務屬性的 Cmdlet，不會從伺服器取得原始屬性，而只會將修改的屬性設定至伺服器。</span><span class="sxs-lookup"><span data-stu-id="6543a-317">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="6543a-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-318">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="6543a-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-319">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="6543a-320">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-320">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-321">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-321">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-322">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-322">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6543a-323">已修正 New-AzStorageAccount 參數 -Kind 預設值的說明問題 [#12189]</span><span class="sxs-lookup"><span data-stu-id="6543a-323">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="6543a-324">已修正新增範例的問題，以顯示如何在 Blob 上傳中設定正確的 ContentType [#12989]</span><span class="sxs-lookup"><span data-stu-id="6543a-324">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="6543a-325">4.7.0 - 2020 年 9 月</span><span class="sxs-lookup"><span data-stu-id="6543a-325">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-326">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-326">Az.Accounts</span></span>
* <span data-ttu-id="6543a-327">已格式化即將推出的重大變更訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-327">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="6543a-328">已將 Azure.Core 更新為 1.4.1</span><span class="sxs-lookup"><span data-stu-id="6543a-328">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-329">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-329">Az.Aks</span></span>
* <span data-ttu-id="6543a-330">已新增 'New-AzAksCluster'、'Set-AzAksCluster' 和 'New-AzAksNodePool' 的用戶端參數驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="6543a-330">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="6543a-331">[#12372]</span><span class="sxs-lookup"><span data-stu-id="6543a-331">[#12372]</span></span>
* <span data-ttu-id="6543a-332">已新增對 'New-AzAksCluster' 中附加元件的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-332">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="6543a-333">[#11239]</span><span class="sxs-lookup"><span data-stu-id="6543a-333">[#11239]</span></span>
* <span data-ttu-id="6543a-334">已為附加元件新增 Cmdlet 'Enable-AzAksAddOn' 和 'Disable-AzAksAddOn'。</span><span class="sxs-lookup"><span data-stu-id="6543a-334">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="6543a-335">[#11239]</span><span class="sxs-lookup"><span data-stu-id="6543a-335">[#11239]</span></span>
* <span data-ttu-id="6543a-336">已為 'New-AzAksCluster' 新增參數 'GenerateSshKey'。</span><span class="sxs-lookup"><span data-stu-id="6543a-336">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="6543a-337">[#12371]</span><span class="sxs-lookup"><span data-stu-id="6543a-337">[#12371]</span></span>
* <span data-ttu-id="6543a-338">已將 api 版本更新為 2020-06-01。</span><span class="sxs-lookup"><span data-stu-id="6543a-338">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-339">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-339">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-340">已顯示特定 API 的其他法律條款。</span><span class="sxs-lookup"><span data-stu-id="6543a-340">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-341">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-341">Az.Compute</span></span>
* <span data-ttu-id="6543a-342">已將 '-EncryptionType' 選擇性參數新增至 'New-AzVmDiskEncryptionSetConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-342">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="6543a-343">適用於新資源類型的新 Cmdlet：DiskAccess 'Get-AzDiskAccess'、'New-AzDiskAccess'、'Get-AzDiskAccess'</span><span class="sxs-lookup"><span data-stu-id="6543a-343">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="6543a-344">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzSnapshotConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-344">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="6543a-345">已將選擇性參數 '-DiskAccessId' 和 '-NetworkAccessPolicy' 新增至 'New-AzDiskConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-345">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="6543a-346">已將 'PatchStatus' 屬性新增至 VirtualMachine 執行個體檢視</span><span class="sxs-lookup"><span data-stu-id="6543a-346">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="6543a-347">已將 'VMHealth' 屬性新增至虛擬機器的執行個體檢視，這是以 '-Status' 叫用 'Get-AzVm' 時傳回的物件</span><span class="sxs-lookup"><span data-stu-id="6543a-347">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="6543a-348">已將 'AssignedHost' 欄位新增至 'Get-AzVM' 和 'Get-AzVmss' 執行個體檢視。</span><span class="sxs-lookup"><span data-stu-id="6543a-348">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="6543a-349">此欄位會顯示虛擬機器執行個體的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6543a-349">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="6543a-350">已將選擇性參數 '-SupportAutomaticPlacement' 新增至 'New-AzHostGroup'</span><span class="sxs-lookup"><span data-stu-id="6543a-350">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="6543a-351">已將 '-HostGroupId' 參數新增至 'New-AzVm' 和 'New-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="6543a-351">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-352">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-352">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-353">已將 ADF .Net SDK 版本更新為 4.11.0</span><span class="sxs-lookup"><span data-stu-id="6543a-353">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-354">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-354">Az.EventHub</span></span>
* <span data-ttu-id="6543a-355">已新增叢集 Cmdlet - 'New-AzEventHubCluster'、'Set-AzEventHubCluster'、'Get-AzEventHubCluster'、'Remove-AzEventHubCluster'、'Get-AzEventHubClustersAvailableRegions'。</span><span class="sxs-lookup"><span data-stu-id="6543a-355">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="6543a-356">已修正問題 #10722：已修正只將 'Listen' 指派給 AuthorizationRule 權限的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-356">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6543a-357">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6543a-357">Az.Functions</span></span>
* <span data-ttu-id="6543a-358">已移除在不支援 v2 函式的區域中建立 v2 函式的功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-358">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="6543a-359">已取代 PowerShell 6.2。</span><span class="sxs-lookup"><span data-stu-id="6543a-359">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="6543a-360">已新增警告，在使用者建立 PowerShell 6.2 函式應用程式時，建議他們改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="6543a-360">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-361">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-361">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-362">支援建立具有自動調整設定的叢集</span><span class="sxs-lookup"><span data-stu-id="6543a-362">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="6543a-363">已將新參數 'v2 Functions' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-363">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="6543a-364">支援操作叢集的自動調整設定</span><span class="sxs-lookup"><span data-stu-id="6543a-364">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="6543a-365">已新增 Cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-365">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6543a-366">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-366">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6543a-367">已新增 Cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-367">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6543a-368">已新增 Cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-368">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="6543a-369">已新增 Cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span><span class="sxs-lookup"><span data-stu-id="6543a-369">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-370">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-370">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-371">已新增對 RBAC 授權的支援 [#10557]</span><span class="sxs-lookup"><span data-stu-id="6543a-371">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="6543a-372">已加強 'Set-AzKeyVaultAccessPolicy' 中的錯誤處理 [#4007]</span><span class="sxs-lookup"><span data-stu-id="6543a-372">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="6543a-373">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="6543a-373">Az.Kusto</span></span>
* <span data-ttu-id="6543a-374">正式發行 'Az.Kusto' 模組</span><span class="sxs-lookup"><span data-stu-id="6543a-374">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-375">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-375">Az.Network</span></span>
* <span data-ttu-id="6543a-376">[重大變更] 已更新下列 Cmdlet 以配合資源虛擬路由器和虛擬中樞</span><span class="sxs-lookup"><span data-stu-id="6543a-376">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="6543a-377">'New-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="6543a-377">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="6543a-378">已新增 -HostedSubnet 參數來支援 IP 設定子資源</span><span class="sxs-lookup"><span data-stu-id="6543a-378">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="6543a-379">已刪除 -HostedGateway 和 -HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="6543a-379">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="6543a-380">'Get-AzVirtualRouter'：</span><span class="sxs-lookup"><span data-stu-id="6543a-380">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="6543a-381">已新增訂用帳戶層級參數集</span><span class="sxs-lookup"><span data-stu-id="6543a-381">Added subscription level parameter set</span></span>
    - <span data-ttu-id="6543a-382">'Remove-AzVirtualRouter'</span><span class="sxs-lookup"><span data-stu-id="6543a-382">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="6543a-383">'Add-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6543a-383">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="6543a-384">'Get-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6543a-384">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="6543a-385">'Remove-AzVirtualRouterPeer'</span><span class="sxs-lookup"><span data-stu-id="6543a-385">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="6543a-386">已新增 Azure 快速路由連接埠的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-386">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="6543a-387">'New-AzExpressRoutePortLOA'</span><span class="sxs-lookup"><span data-stu-id="6543a-387">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="6543a-388">已將 RemoteBgpCommunities 屬性新增至 VirtualNetwork 對等互連資源</span><span class="sxs-lookup"><span data-stu-id="6543a-388">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="6543a-389">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-389">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="6543a-390">已將 VpnGatewayIpConfigurations 新增至 'Get-AzVpnGateway' 輸出</span><span class="sxs-lookup"><span data-stu-id="6543a-390">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="6543a-391">已修正 'Set-AzApplicationGatewaySslCertificate' 的錯誤 (bug) [#9488]</span><span class="sxs-lookup"><span data-stu-id="6543a-391">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="6543a-392">已將 'AllowActiveFTP' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="6543a-392">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="6543a-393">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上啟用網際網路安全性設定/移除。</span><span class="sxs-lookup"><span data-stu-id="6543a-393">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="6543a-394">已更新 'New-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag'，可讓客戶將其設定為 true，以在 P2SVpnGateway 上啟用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="6543a-394">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="6543a-395">已更新 'Update-AzP2sVpnGateway'：已新增選擇性切換參數 'EnableInternetSecurityFlag' 或 'DisableInternetSecurityFlag'，可讓客戶將其設定為 true/false，以在 P2SVpnGateway 上啟用/停用網際網路安全性，這將適用於點對站用戶端。</span><span class="sxs-lookup"><span data-stu-id="6543a-395">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="6543a-396">已新增 Cmdlet 'Reset-AzP2sVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan P2SVpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="6543a-396">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="6543a-397">已新增 Cmdlet 'Reset-AzVpnGateway'，可讓客戶重設/重新啟動其 VirtualWan VpnGateway 進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="6543a-397">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="6543a-398">已更新 'Set-AzVirtualNetworkSubnetConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-398">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="6543a-399">如果已在參數中明確設定，請將子網路的 NSG 和路由表屬性設定為 null [#1548][#9718]</span><span class="sxs-lookup"><span data-stu-id="6543a-399">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-400">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-401">已修正工作負載備份項目的刪除狀態。</span><span class="sxs-lookup"><span data-stu-id="6543a-401">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-402">Az.Resources</span></span>
* <span data-ttu-id="6543a-403">已新增 Set-AzRoleAssignment 的遺漏檢查</span><span class="sxs-lookup"><span data-stu-id="6543a-403">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="6543a-404">已將重大變更屬性新增至 'Get-AzResourceGroupDeploymentOperation' 的 'SubscriptionId' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-404">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="6543a-405">已更新 ARM 範本 What-If Cmdlet，以顯示「忽略」上次資源變更</span><span class="sxs-lookup"><span data-stu-id="6543a-405">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="6543a-406">已修正部署 Cmdlet 的安全和陣列參數序列化問題 [#12773]</span><span class="sxs-lookup"><span data-stu-id="6543a-406">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-407">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-408">已新增適用於受控叢集和節點類型的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-408">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="6543a-409">'New-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-409">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6543a-410">'Get-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-410">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6543a-411">'Set-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-411">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6543a-412">'Remove-AzServiceFabricManagedCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-412">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="6543a-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="6543a-413">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="6543a-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span><span class="sxs-lookup"><span data-stu-id="6543a-414">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="6543a-415">'New-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6543a-415">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6543a-416">'Get-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6543a-416">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6543a-417">'Set-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6543a-417">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6543a-418">'Remove-AzServiceFabricManagedNodeType'</span><span class="sxs-lookup"><span data-stu-id="6543a-418">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="6543a-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-419">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="6543a-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span><span class="sxs-lookup"><span data-stu-id="6543a-420">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="6543a-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-421">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="6543a-422">'Restart-AzServiceFabricManagedNodeTyp'</span><span class="sxs-lookup"><span data-stu-id="6543a-422">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="6543a-423">已將 Service Fabric SDK 升級為版本 1.2.0，此版本將服務網狀架構資源提供者 api-version 2020-03-01 用於目前模型，以及將 2020-01-01-preview 用於受控叢集。</span><span class="sxs-lookup"><span data-stu-id="6543a-423">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-424">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-424">Az.Sql</span></span>
* <span data-ttu-id="6543a-425">已將 BackupStorageRedundancy 新增至 'New-AzSqlInstance' 及 'Get-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="6543a-425">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="6543a-426">已新增 Cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-426">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-427">已新增 Cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-427">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-428">已將 Force 參數新增至 'New-AzSqlInstance'</span><span class="sxs-lookup"><span data-stu-id="6543a-428">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="6543a-429">已新增受控資料庫記錄重新執行服務的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-429">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="6543a-430">'Start-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6543a-430">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6543a-431">'Get-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6543a-431">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6543a-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6543a-432">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="6543a-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span><span class="sxs-lookup"><span data-stu-id="6543a-433">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="6543a-434">已新增 Cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-434">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-435">已新增 Cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-435">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-436">已新增 Cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-436">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-437">已更新 Cmdlet 'New-AzSqlDatabaseImport' 和 'New-AzSqlDatabaseExport' 以支援網路隔離功能</span><span class="sxs-lookup"><span data-stu-id="6543a-437">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="6543a-438">已新增 Cmdlet 'New-AzSqlDatabaseImportExisting'</span><span class="sxs-lookup"><span data-stu-id="6543a-438">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="6543a-439">已更新資料庫 Cmdlet 以支援備份儲存體類型規格</span><span class="sxs-lookup"><span data-stu-id="6543a-439">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="6543a-440">已將 Force 參數新增至 'New-AzSqlDatabase'</span><span class="sxs-lookup"><span data-stu-id="6543a-440">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="6543a-441">已 'New-AzSqlDatabase' 的選取區域中新增 BackupStorageRedundancy 設定的警告</span><span class="sxs-lookup"><span data-stu-id="6543a-441">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="6543a-442">已更新伺服器和執行個體的 ActiveDirectoryOnlyAuthentication Cmdlet，以包含 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="6543a-442">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-443">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-443">Az.Storage</span></span>
* <span data-ttu-id="6543a-444">已升級至 Microsoft.Azure.Storage.DataMovement 2.0.0 來修正上傳 blob 失敗 [#12220]</span><span class="sxs-lookup"><span data-stu-id="6543a-444">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="6543a-445">支援時間點還原</span><span class="sxs-lookup"><span data-stu-id="6543a-445">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="6543a-446">'Enable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-446">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-447">'Disable-AzStorageBlobRestorePolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-447">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="6543a-448">'New-AzStorageBlobRangeToRestore'</span><span class="sxs-lookup"><span data-stu-id="6543a-448">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="6543a-449">'Restore-AzStorageBlobRange'</span><span class="sxs-lookup"><span data-stu-id="6543a-449">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="6543a-450">支援執行 get-AzureRMStorageAccount 搭配參數 -IncludeGeoReplicationStats，取得儲存體帳戶的 blob 還原狀態</span><span class="sxs-lookup"><span data-stu-id="6543a-450">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="6543a-451">'Get-AzureRMStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-451">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="6543a-452">已為即將進行的 Cmdlet 輸出變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-452">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="6543a-453">'Get-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-453">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="6543a-454">'Set-AzStorageContainerStoredAccessPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-454">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="6543a-455">'Set-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-455">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6543a-456">'Get-AzStorageAccountManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-456">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="6543a-457">'Add-AzStorageAccountManagementPolicyAction'</span><span class="sxs-lookup"><span data-stu-id="6543a-457">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="6543a-458">'New-AzStorageAccountManagementPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6543a-458">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="6543a-459">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.8</span><span class="sxs-lookup"><span data-stu-id="6543a-459">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="6543a-460">感謝我們的社群參與者</span><span class="sxs-lookup"><span data-stu-id="6543a-460">Thanks to our community contributors</span></span>
* <span data-ttu-id="6543a-461">Thomas Van Laere (@ThomVanL)，新增 Dockerfile-alpine-3.10 (#12911)</span><span class="sxs-lookup"><span data-stu-id="6543a-461">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="6543a-462">Lohith Chowdary Chilukuri (@Lochiluk)，更新 Remove-AzNetworkInterfaceIpConfig.md (#12807)</span><span class="sxs-lookup"><span data-stu-id="6543a-462">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="6543a-463">Roberth Strand (@roberthstrand)，Get-AzResourceGroup - 新範例和清除 (#12828)</span><span class="sxs-lookup"><span data-stu-id="6543a-463">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="6543a-464">Ravi Mishra (@inmishrar)，將 Azure Web 應用程式執行階段堆疊更新為 DOTNETCORE (#12833)</span><span class="sxs-lookup"><span data-stu-id="6543a-464">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="6543a-465">@jack-education，更新 New-azvirtualnetworksubnetconfig 以允許從子網移除 NSG 和路由表 (#12351)</span><span class="sxs-lookup"><span data-stu-id="6543a-465">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="6543a-466">@hagop-globanet，更新 Add-AzApplicationGatewayCustomError.md (#12784)</span><span class="sxs-lookup"><span data-stu-id="6543a-466">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="6543a-467">Joshua Van Daalen (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="6543a-467">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="6543a-468">將 Property 的拼寫更新為 Property (#12821)</span><span class="sxs-lookup"><span data-stu-id="6543a-468">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="6543a-469">更新 New-AzResourceLock.md 範例 (#12806)</span><span class="sxs-lookup"><span data-stu-id="6543a-469">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="6543a-470">Eragon Riddle (@eragonriddle)，更正範例中的參數欄位名稱 (#12825)</span><span class="sxs-lookup"><span data-stu-id="6543a-470">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="6543a-471">@rossifumax，修正 New-AzConfigurationAssignment.md 中的錯字 (#12701)</span><span class="sxs-lookup"><span data-stu-id="6543a-471">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="6543a-472">4.6.1 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="6543a-472">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="6543a-473">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-473">Az.Compute</span></span>
* <span data-ttu-id="6543a-474">已修補 'New-AzVm' 中的 '-EncryptionAtHost' 參數，以移除預設值 false [#12776]</span><span class="sxs-lookup"><span data-stu-id="6543a-474">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="6543a-475">4.6.0 - 2020 年8 月</span><span class="sxs-lookup"><span data-stu-id="6543a-475">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-476">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-476">Az.Accounts</span></span>
* <span data-ttu-id="6543a-477">當探索端點未傳回預設 AzureCloud 或其他公用環境時，載入所有公用雲端環境 [#12633]</span><span class="sxs-lookup"><span data-stu-id="6543a-477">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="6543a-478">在 'Get-AzSubscription' 中公開 SubscriptionPolicies [#12551]</span><span class="sxs-lookup"><span data-stu-id="6543a-478">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-479">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-479">Az.Automation</span></span>
* <span data-ttu-id="6543a-480">已將 '-RunOn' 參數新增至 'Set-AzAutomationWebhook，以指定混合式背景工作角色群組</span><span class="sxs-lookup"><span data-stu-id="6543a-480">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-481">Az.Compute</span></span>
* <span data-ttu-id="6543a-482">已將 '-EncryptionAtHost' 參數新增至 'New-AzVm'、'New-AzVmss'、'New-AzVMConfig'、'New-AzVmssConfig'、'Update-AzVM' 及 'Update-AzVmss'</span><span class="sxs-lookup"><span data-stu-id="6543a-482">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="6543a-483">已將 'SecurityProfile' 新增至 'Get-AzVM' 和 'Get-AzVmss' 傳回物件</span><span class="sxs-lookup"><span data-stu-id="6543a-483">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="6543a-484">已將 '-InstanceView' 參數新增為 'Get-AzHostGroup' 的選擇性參數</span><span class="sxs-lookup"><span data-stu-id="6543a-484">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="6543a-485">已新增 'Invoke-AzVmPatchAssessment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-485">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-486">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-486">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-487">已將遺漏屬性新增至 PSPipelineRun 類別。</span><span class="sxs-lookup"><span data-stu-id="6543a-487">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-488">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-488">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-489">支援建立具有主機加密功能的叢集。</span><span class="sxs-lookup"><span data-stu-id="6543a-489">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-490">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-490">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-491">已新增打算停用虛刪除的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-491">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="6543a-492">已新增打算移除 SecretValueText 屬性的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-492">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="6543a-493">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="6543a-493">Az.Maintenance</span></span>
* <span data-ttu-id="6543a-494">已將選擇性的排程相關欄位新增至 'New-AzMaintenanceConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-494">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="6543a-495">已為 'Get-AzMaintenancePublicConfiguration' 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-495">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6543a-496">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6543a-496">Az.ManagedServices</span></span>
* <span data-ttu-id="6543a-497">已在受控服務指派和定義的 Cmdlet 上新增中斷性變更警告</span><span class="sxs-lookup"><span data-stu-id="6543a-497">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-498">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-498">Az.Monitor</span></span>
* <span data-ttu-id="6543a-499">已擴充 'Set-AzDiagnosticSetting' 中設定的參數，以分隔記錄和計量啟用 [#12482]</span><span class="sxs-lookup"><span data-stu-id="6543a-499">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="6543a-500">已修正從管線取得計量警示時的 'Add-AzMetricAlertRuleV2' 錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-500">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-501">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-501">Az.Resources</span></span>
* <span data-ttu-id="6543a-502">已更新 'Get-AzPolicyAlias' 回應以包含指出別名是否可由 Azure 原則修改的資訊。</span><span class="sxs-lookup"><span data-stu-id="6543a-502">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="6543a-503">已建立新的 'Set-AzRoleAssignment' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-503">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="6543a-504">已新增 'Get-AzDeploymentManagementGroupWhatIfResult'，以取得 ARM 範本在管理群組範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="6543a-504">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="6543a-505">已新增 'Get-AzTenantWhatIfResult' Cmdlet，以取得 ARM 範本在租使用者範圍的假設結果</span><span class="sxs-lookup"><span data-stu-id="6543a-505">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="6543a-506">已覆寫 'New-AzManagementGroupDeployment' 和 'New-AzTenantDeployment' 的 '-WhatIf' 和 '-Confirm'，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="6543a-506">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="6543a-507">已修正新部署 Cmdlet 的 '-WhatIf' 和 '-Confirm' 行為，使其符合 False 和</span><span class="sxs-lookup"><span data-stu-id="6543a-507">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="6543a-508">已修正 '-TemplateObject' 和 'TemplateParameterObject' 的序列化錯誤 [#1528] [#6292]</span><span class="sxs-lookup"><span data-stu-id="6543a-508">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="6543a-509">已針對即將進行的輸出類型變更，對 'Get-AzResourceGroupDeploymentOperation' 新增中斷性變更屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-509">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6543a-510">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6543a-510">Az.SignalR</span></span>
* <span data-ttu-id="6543a-511">已修正 'Restart-AzSignalR' 和 'Update-AzSignalR' 說明檔錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-511">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="6543a-512">已新增 'Update-AzSignalRNetworkAcl'、'Set-AzSignalRUpstream' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-512">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-513">Az.Storage</span></span>
* <span data-ttu-id="6543a-514">支援的 Blob 查詢加速</span><span class="sxs-lookup"><span data-stu-id="6543a-514">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="6543a-515">'Get-AzStorageBlobQueryResult'</span><span class="sxs-lookup"><span data-stu-id="6543a-515">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="6543a-516">'New-AzStorageBlobQueryConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-516">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="6543a-517">已更新說明檔、新增更多描述及修正錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-517">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="6543a-518">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="6543a-518">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="6543a-519">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-519">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="6543a-520">已修正當相關子目錄不存在時，下載 Blob 會失敗的問題 [#12592]</span><span class="sxs-lookup"><span data-stu-id="6543a-520">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="6543a-521">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-521">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="6543a-522">支援在儲存體帳戶上設定/取得/移除物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="6543a-522">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="6543a-523">'New-AzStorageObjectReplicationPolicyRule'</span><span class="sxs-lookup"><span data-stu-id="6543a-523">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="6543a-524">'Set-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-524">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="6543a-525">'Get-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-525">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="6543a-526">'Remove-AzStorageObjectReplicationPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-526">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="6543a-527">支援在儲存體帳戶的 Blob 服務上啟用/停用 ChangeFeed</span><span class="sxs-lookup"><span data-stu-id="6543a-527">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="6543a-528">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-528">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="6543a-529">4.5.0 - 2020 年 8 月</span><span class="sxs-lookup"><span data-stu-id="6543a-529">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-530">Az.Accounts</span></span>
* <span data-ttu-id="6543a-531">已將 'Connect-AzAccount' 更新為接受參數 'MaxContextPopulation' [#9865]</span><span class="sxs-lookup"><span data-stu-id="6543a-531">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="6543a-532">已將 SubscriptionClient 版本更新為 2019-06-01 並顯示租用戶網域 [#9838]</span><span class="sxs-lookup"><span data-stu-id="6543a-532">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="6543a-533">訂用帳戶支援的主租用戶和 managedBy 租用戶資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-533">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="6543a-534">已更正遙測資料中的模組名稱、版本資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-534">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="6543a-535">已調整 SqlDatabaseDnsSuffix 和 ServiceManagementUrl (如果環境中繼資料端點傳回不相容的值)</span><span class="sxs-lookup"><span data-stu-id="6543a-535">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-536">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-536">Az.Aks</span></span>
* <span data-ttu-id="6543a-537">已將 'ClientIdAndSecret' 移除至 'ServicePrincipalIdAndSecret' 並將 'ClientIdAndSecret' 設定為別名 [#12381]。</span><span class="sxs-lookup"><span data-stu-id="6543a-537">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="6543a-538">已將 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' 移除至 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' 並將原始項目設定為別名 [#12373]。</span><span class="sxs-lookup"><span data-stu-id="6543a-538">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-539">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-539">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-540">已新增新的 'Add-AzApiManagementApiToGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-540">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-541">已新增新的 'Get-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-541">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-542">已新增新的 'Get-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-542">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6543a-543">已新增新的 'Get-AzApiManagementGatewayKey' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-543">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="6543a-544">已新增新的 'New-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-544">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-545">已新增新的 'New-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-545">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6543a-546">已新增新的 'New-AzApiManagementResourceLocationObject' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-546">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="6543a-547">已新增新的 'Remove-AzApiManagementApiFromGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-547">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-548">已新增新的 'Remove-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-548">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-549">已新增新的 'Remove-AzApiManagementGatewayHostnameConfiguration' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-549">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="6543a-550">已新增新的 'Update-AzApiManagementGateway' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-550">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="6543a-551">已將新的選擇性 [-GatewayId] 參數新增至 'Get-AzApiManagementApi' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-551">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-552">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-552">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-553">已特別將 'Deny' 作為 NetworkRules 預設動作使用。</span><span class="sxs-lookup"><span data-stu-id="6543a-553">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-554">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-554">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-555">已修正當 Enum.Parse 嘗試將 Null 值強制轉型為 Enabled 或 Disabled 列舉值時擲回例外狀況的問題 [#12344]</span><span class="sxs-lookup"><span data-stu-id="6543a-555">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-556">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-556">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-557">支援使用傳輸中加密功能建立叢集。</span><span class="sxs-lookup"><span data-stu-id="6543a-557">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="6543a-558">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-558">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="6543a-559">將新參數 'EncryptionInTransit' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-559">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="6543a-560">支援使用私人連結功能建立叢集：</span><span class="sxs-lookup"><span data-stu-id="6543a-560">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="6543a-561">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightCluster'</span><span class="sxs-lookup"><span data-stu-id="6543a-561">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="6543a-562">將新參數 'PublicNetworkAccessType' 和 'OutboundPublicNetworkAccessType' 新增至 Cmdlet 'New-AzHDInsightClusterConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-562">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="6543a-563">呼叫 'New-AzHDInsightCluster' 或 'Get-AzHDInsightCluster' 時傳回了虛擬網路資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-563">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-564">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-564">Az.Network</span></span>
* <span data-ttu-id="6543a-565">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-565">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="6543a-566">已新增不中斷變更：'Remove-AzExpressRouteCircutPeeringConfig' 中私人對等互連的 PeerAddressType 功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-566">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="6543a-567">程式碼已變更為忽略 AddressPrefixType 和 PeerAddressType 參數的大小寫。</span><span class="sxs-lookup"><span data-stu-id="6543a-567">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="6543a-568">已修改 'New-AzLoadBalancerFrontendIpConfig'、'New-AzPublicIpAddress' 和 'New-AzPublicIpPrefix' 的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-568">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-569">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-569">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-570">已新增 'Remove-AzOperationalInsightsworkspace' 的 '-ForceDelete' 選項</span><span class="sxs-lookup"><span data-stu-id="6543a-570">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="6543a-571">已新增新的 Cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span><span class="sxs-lookup"><span data-stu-id="6543a-571">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="6543a-572">已新增新的 Cmdlet 'Restore-AzOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="6543a-572">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-573">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-574">已改善 Azure 備份容器/項目探索體驗。</span><span class="sxs-lookup"><span data-stu-id="6543a-574">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-575">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-575">Az.Resources</span></span>
* <span data-ttu-id="6543a-576">已將 'Condition'、'ConditionVersion' 和 'Description' 屬性新增至 'New-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="6543a-576">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="6543a-577">這包括資料模型的所有相關變更</span><span class="sxs-lookup"><span data-stu-id="6543a-577">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-578">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-578">Az.Sql</span></span>
* <span data-ttu-id="6543a-579">已修正 'New-AzSqlServer' 和 'Set-AzSqlServer' 中可能的伺服器名稱不區分大小寫錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-579">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="6543a-580">已修正 'New-AzSqlDatabaseSecondary' 中現有資料庫錯誤上傳回的錯誤資料庫名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-580">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-581">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-581">Az.Storage</span></span>
* <span data-ttu-id="6543a-582">支援建立具有新權限 x、t 的容器/blob Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-582">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="6543a-583">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="6543a-583">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="6543a-584">'New-AzStorageContainerSASToken'</span><span class="sxs-lookup"><span data-stu-id="6543a-584">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="6543a-585">支援建立具有新權限 x、t、f 的帳戶 Sas 權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-585">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="6543a-586">'New-AzStorageAccountSASToken'</span><span class="sxs-lookup"><span data-stu-id="6543a-586">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="6543a-587">支援取得單一檔案共用使用方式</span><span class="sxs-lookup"><span data-stu-id="6543a-587">Supported get single file share usage</span></span>
    - <span data-ttu-id="6543a-588">'Get-AzRmStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-588">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="6543a-589">4.4.0 - 2020 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6543a-589">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-590">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-590">Az.Accounts</span></span>
* <span data-ttu-id="6543a-591">已新增新的 Cmdlet 'Invoke-AzRestMethod'</span><span class="sxs-lookup"><span data-stu-id="6543a-591">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="6543a-592">已修正在多處理序案例中可能導致驗證錯誤的問題，例如使用 'Start-Job' 執行多個 Azure PowerShell Cmdlet [#9448]</span><span class="sxs-lookup"><span data-stu-id="6543a-592">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-593">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-593">Az.Aks</span></span>
* <span data-ttu-id="6543a-594">已修正 'Get-AzAks' 無法取得所有叢集的錯誤 (bug) [#12296]</span><span class="sxs-lookup"><span data-stu-id="6543a-594">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-595">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-595">Az.AnalysisServices</span></span>
* <span data-ttu-id="6543a-596">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="6543a-596">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-597">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-597">Az.Automation</span></span>
* <span data-ttu-id="6543a-598">已修正具有 escape 字元的字串無法轉換成 json 物件的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-598">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-599">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-599">Az.Compute</span></span>
* <span data-ttu-id="6543a-600">在沒有 'latest' 映像版本的情況下使用 'New-AzVmss' 時，新增警告</span><span class="sxs-lookup"><span data-stu-id="6543a-600">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-601">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-601">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-602">已將全域參數新增至 Data Factory。</span><span class="sxs-lookup"><span data-stu-id="6543a-602">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6543a-603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6543a-603">Az.EventGrid</span></span>
* <span data-ttu-id="6543a-604">已更新為使用 2020-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6543a-604">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="6543a-605">加入新功能：</span><span class="sxs-lookup"><span data-stu-id="6543a-605">Added new features:</span></span>
    - <span data-ttu-id="6543a-606">輸入對應</span><span class="sxs-lookup"><span data-stu-id="6543a-606">Input mapping</span></span>
    - <span data-ttu-id="6543a-607">事件傳遞結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-607">Event Delivery Schema</span></span>
    - <span data-ttu-id="6543a-608">私人連結</span><span class="sxs-lookup"><span data-stu-id="6543a-608">Private Link</span></span>
    - <span data-ttu-id="6543a-609">雲端事件 V10 結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-609">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="6543a-610">將服務匯流排主題作為目的地</span><span class="sxs-lookup"><span data-stu-id="6543a-610">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="6543a-611">將 Azure Function 作為目的地</span><span class="sxs-lookup"><span data-stu-id="6543a-611">Azure Function As Destination</span></span>
    - <span data-ttu-id="6543a-612">WebHook 批次處理</span><span class="sxs-lookup"><span data-stu-id="6543a-612">WebHook Batching</span></span>
    - <span data-ttu-id="6543a-613">安全 Webhook (AAD 支援)</span><span class="sxs-lookup"><span data-stu-id="6543a-613">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="6543a-614">IpFiltering</span><span class="sxs-lookup"><span data-stu-id="6543a-614">IpFiltering</span></span>
* <span data-ttu-id="6543a-615">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-615">Updated cmdlets:</span></span>
    - <span data-ttu-id="6543a-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span><span class="sxs-lookup"><span data-stu-id="6543a-616">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="6543a-617">新增選擇性參數以支援 webhook 批次處理。</span><span class="sxs-lookup"><span data-stu-id="6543a-617">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="6543a-618">新增選擇性參數以使用 AAD 支援安全的 Wdblook。</span><span class="sxs-lookup"><span data-stu-id="6543a-618">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="6543a-619">為 EndpointType 參數新增新的列舉，以支援 Azure 函式和服務匯流排主題作為新的目的地。</span><span class="sxs-lookup"><span data-stu-id="6543a-619">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="6543a-620">為傳遞結構描述新增選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-620">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="6543a-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' 和 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="6543a-621">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="6543a-622">新增選擇性參數以支援 IpFiltering。</span><span class="sxs-lookup"><span data-stu-id="6543a-622">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="6543a-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span><span class="sxs-lookup"><span data-stu-id="6543a-623">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="6543a-624">新增選擇性參數以支援輸入對應。</span><span class="sxs-lookup"><span data-stu-id="6543a-624">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-625">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-625">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-626">已更新模組以使用 API 2020-05-01</span><span class="sxs-lookup"><span data-stu-id="6543a-626">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="6543a-627">已新增對儲存體、Keyvault 和 Web App Service 資源的私人連結支援</span><span class="sxs-lookup"><span data-stu-id="6543a-627">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-628">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-628">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-629">支援在國家雲端中建立具有 ADLSGen1/2 儲存體的叢集。</span><span class="sxs-lookup"><span data-stu-id="6543a-629">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-630">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-630">Az.Monitor</span></span>
* <span data-ttu-id="6543a-631">已修正計量或記錄為 Null 時，'Get-AzDiagnosticSetting' 的錯誤 (bug) [#12272]</span><span class="sxs-lookup"><span data-stu-id="6543a-631">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-632">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-632">Az.Network</span></span>
* <span data-ttu-id="6543a-633">已修正 VWan HubVnet 連線中的參數交換</span><span class="sxs-lookup"><span data-stu-id="6543a-633">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="6543a-634">為 Azure 網路虛擬設備網站新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-634">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="6543a-635">'Get-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6543a-635">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6543a-636">'New-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6543a-636">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6543a-637">'Remove-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6543a-637">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6543a-638">'Update-AzVirtualApplianceSite'</span><span class="sxs-lookup"><span data-stu-id="6543a-638">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="6543a-639">'New-AzOffice365PolicyProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-639">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="6543a-640">為 Azure 網路虛擬設備新增了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-640">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="6543a-641">'Get-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6543a-641">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6543a-642">'New-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6543a-642">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6543a-643">'Remove-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6543a-643">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6543a-644">'Update-AzNetworkVirtualAppliance'</span><span class="sxs-lookup"><span data-stu-id="6543a-644">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="6543a-645">'Get-AzNetworkVirtualApplianceSku'</span><span class="sxs-lookup"><span data-stu-id="6543a-645">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="6543a-646">'New-AzVirtualApplianceSkuProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-646">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="6543a-647">將應用程式閘道上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-647">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="6543a-648">將 StorageSync 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-648">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="6543a-649">將 SignalR 上架至私人連結通用 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-649">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-650">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-650">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-651">已移除驗證的專案參考</span><span class="sxs-lookup"><span data-stu-id="6543a-651">Removed project reference to Authentication</span></span>
* <span data-ttu-id="6543a-652">Azure 備份微調的 Cmdlet 有助於文字更精確。</span><span class="sxs-lookup"><span data-stu-id="6543a-652">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="6543a-653">Azure 備份新增了使用 'Get-AzRecoveryServicesBackupJob' Cmdlet 來擷取 MAB 代理程式作業的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-653">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-654">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-654">Az.Resources</span></span>
* <span data-ttu-id="6543a-655">已將 'Save-AzResourceGroupDeploymentTemplate' 更新為使用 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-655">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="6543a-656">已新增 'Unregister-AzResourceProvider' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-656">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-657">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-657">Az.Sql</span></span>
* <span data-ttu-id="6543a-658">在 'Set-AzSqlInstanceActiveDirectoryAdministrator' Cmdlet 中新增了服務主體和來賓使用者的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-658">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="6543a-659">已修正資料分類 Cmdlet 中的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-659">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="6543a-660">已新增 Azure SQL 受控執行個體容錯移轉的支援：'Invoke-AzSqlInstanceFailover'</span><span class="sxs-lookup"><span data-stu-id="6543a-660">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-661">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-661">Az.Storage</span></span>
* <span data-ttu-id="6543a-662">已修正未針對某些資料平面 Cmdlet 新增 UserAgent 的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-662">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="6543a-663">支援具有 MinimumTlsVersion 和 AllowBlobPublicAccess 的建立/更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-663">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="6543a-664">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-664">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="6543a-665">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-665">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-666">支援在儲存體帳戶的 Blob 服務上啟用/停用版本控制</span><span class="sxs-lookup"><span data-stu-id="6543a-666">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="6543a-667">'Update-AzStorageBlobServiceProperty'</span><span class="sxs-lookup"><span data-stu-id="6543a-667">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="6543a-668">支援 Blob 版本的列出 Blob</span><span class="sxs-lookup"><span data-stu-id="6543a-668">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="6543a-669">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6543a-669">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="6543a-670">支援取得/移除單一 Blob 快照集或 Blob 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-670">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="6543a-671">'Get-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6543a-671">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="6543a-672">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6543a-672">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="6543a-673">支援從 Azure.Storage.Blobs V12 所產生的 Blob 物件管道</span><span class="sxs-lookup"><span data-stu-id="6543a-673">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="6543a-674">'Get-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-674">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="6543a-675">'New-AzStorageBlobSASToken'</span><span class="sxs-lookup"><span data-stu-id="6543a-675">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="6543a-676">'Remove-AzStorageBlob'</span><span class="sxs-lookup"><span data-stu-id="6543a-676">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="6543a-677">'Set-AzStorageBlobContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-677">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="6543a-678">'Start-AzStorageBlobCopy'</span><span class="sxs-lookup"><span data-stu-id="6543a-678">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6543a-679">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6543a-679">Az.StorageSync</span></span>
* <span data-ttu-id="6543a-680">新增了以 ApiVersion 2020-03-01 為目標的新版 StorageSync SDK</span><span class="sxs-lookup"><span data-stu-id="6543a-680">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="6543a-681">已新增更新儲存體同步服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-681">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="6543a-682">'Set-AzStorageSyncService'</span><span class="sxs-lookup"><span data-stu-id="6543a-682">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="6543a-683">已將 IncomingTrafficPolicy 和 PrivateEndpointConnections 新增至 StorageSyncService Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-683">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-684">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-684">Az.Websites</span></span>
* <span data-ttu-id="6543a-685">已新增支援而可針對未和 App Service 方案位於相同資源群組中的插槽執行作業</span><span class="sxs-lookup"><span data-stu-id="6543a-685">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="6543a-686">4.3.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6543a-686">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-687">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-687">Az.Accounts</span></span>
* <span data-ttu-id="6543a-688">預設支援的探索環境設定，並透過 'Add-AzEnvironment' 新增環境</span><span class="sxs-lookup"><span data-stu-id="6543a-688">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="6543a-689">更新預先載入的組件 [#12024]、[#11976]</span><span class="sxs-lookup"><span data-stu-id="6543a-689">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="6543a-690">已更新 Azure.Core 組件</span><span class="sxs-lookup"><span data-stu-id="6543a-690">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="6543a-691">已修正可能導致 'Connect-AzAccount' 在多執行緒執行中失敗的問題 [#11201]</span><span class="sxs-lookup"><span data-stu-id="6543a-691">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-692">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-692">Az.Aks</span></span>
* <span data-ttu-id="6543a-693">透過對 [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) 和 [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) API 的呼叫，取代舊 [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) 的使用方式</span><span class="sxs-lookup"><span data-stu-id="6543a-693">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-694">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-694">Az.Batch</span></span>
* <span data-ttu-id="6543a-695">已將 Az.Batch 更新為使用 'Microsoft.Azure.Management.Batch' SDK 版本 11.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-695">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="6543a-696">新增在 'New-AzBatchAccount' Cmdlet 中設定 BatchAccount 身分識別的功能</span><span class="sxs-lookup"><span data-stu-id="6543a-696">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-697">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-698">支援的顯示帳戶功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-698">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="6543a-699">支援修改 PublicNetworkAccess。</span><span class="sxs-lookup"><span data-stu-id="6543a-699">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-700">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-700">Az.Compute</span></span>
* <span data-ttu-id="6543a-701">已將 SimulateEviction 參數新增至 Set-AzVM 和 Set-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-701">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="6543a-702">已將 'Premium_LRS' 新增至 New-AzGalleryImageVersion Cmdlet 的 StorageAccountType 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="6543a-702">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="6543a-703">已將子狀態新增至 VMCustomScriptExtension [#11297]</span><span class="sxs-lookup"><span data-stu-id="6543a-703">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="6543a-704">已將 'Delete' 新增至 New-AzVM 和 New-AzVMConfig Cmdlet 的 EvictionPolicy 參數的引數完成器。</span><span class="sxs-lookup"><span data-stu-id="6543a-704">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="6543a-705">已修正適用於 SAP 的新 VM 擴充功能名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-705">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-706">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-706">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-707">已將 ADF .Net SDK 版本更新為 4.9.0</span><span class="sxs-lookup"><span data-stu-id="6543a-707">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-708">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-708">Az.EventHub</span></span>
* <span data-ttu-id="6543a-709">已將受控識別參數新增至 'New-AzEventHubNamespace' 和 'Set-AzEventHubNamespace' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-709">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6543a-710">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6543a-710">Az.Functions</span></span>
* <span data-ttu-id="6543a-711">已新增建立 PowerShell 7.0 和 Java 11 函式應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-711">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-712">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-712">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-713">支援的清單主機和重新開機 HDInsight 叢集的特定主機。</span><span class="sxs-lookup"><span data-stu-id="6543a-713">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6543a-714">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6543a-714">Az.HealthcareApis</span></span>
* <span data-ttu-id="6543a-715">已將 SDK 版本更新為 1.1.0</span><span class="sxs-lookup"><span data-stu-id="6543a-715">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="6543a-716">已新增匯出設定和受控識別的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-716">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-717">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-717">Az.Monitor</span></span>
* <span data-ttu-id="6543a-718">已修正 'Set-AzActivityLogAlert' 的輸入物件參數</span><span class="sxs-lookup"><span data-stu-id="6543a-718">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="6543a-719">已修正 'Set-AzActionGroup' 的 'InputObject' 參數 [#10868]</span><span class="sxs-lookup"><span data-stu-id="6543a-719">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-720">Az.Network</span></span>
* <span data-ttu-id="6543a-721">已將 AddressPrefixType 參數的支援新增至 'Remove-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-721">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="6543a-722">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-722">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="6543a-723">'New-AzFirewallPolicyDnsSetting'</span><span class="sxs-lookup"><span data-stu-id="6543a-723">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="6543a-724">在防火牆原則的網路規則中支援目的地 FQDN</span><span class="sxs-lookup"><span data-stu-id="6543a-724">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="6543a-725">已新增對後端位址集區作業的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-725">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="6543a-726">'New-AzLoadBalancerBackendAddressConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-726">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="6543a-727">'New-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6543a-727">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6543a-728">'Set-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6543a-728">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6543a-729">'Remove-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6543a-729">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="6543a-730">'Get-AzLoadBalancerBackendAddressPool'</span><span class="sxs-lookup"><span data-stu-id="6543a-730">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="6543a-731">已新增 ' New-AzIpGroup' 的名稱驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-731">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="6543a-732">已新增 Azure FirewallPolicy 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-732">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="6543a-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span><span class="sxs-lookup"><span data-stu-id="6543a-733">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="6543a-734">已更新下列功能命令：在 VirtualWan P2SVpnGateway 上設定/移除自訂 dns 伺服器。</span><span class="sxs-lookup"><span data-stu-id="6543a-734">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="6543a-735">已更新 New-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="6543a-735">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="6543a-736">已更新 Update-AzP2sVpnGateway：已為客戶新增選擇性參數 '-CustomDnsServer'，以指定要在 P2SVpnGateway 上設定的 dns 伺服器 (可供點對站用戶端使用)。</span><span class="sxs-lookup"><span data-stu-id="6543a-736">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="6543a-737">已更新 'Update-AzVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-737">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="6543a-738">已為客戶新增選擇性參數 '-BgpPeeringAddress'，以指定要在 VpnGateway 上設定的自訂 bgps。</span><span class="sxs-lookup"><span data-stu-id="6543a-738">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="6543a-739">已新增新的 Cmdlet，以支援重設 VirtualHub 資源的路由狀態：</span><span class="sxs-lookup"><span data-stu-id="6543a-739">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="6543a-740">'Reset-AzHubRouter'</span><span class="sxs-lookup"><span data-stu-id="6543a-740">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="6543a-741">已根據防火牆原則的最近 Swagger 變更更新下列事項</span><span class="sxs-lookup"><span data-stu-id="6543a-741">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="6543a-742">變更 RuleGroup、RuleCollectionGroup 和 RuleType 的名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-742">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="6543a-743">已新增對防火牆原則 NAT 規則集合的支援，以支援多個 NAT 規則集合</span><span class="sxs-lookup"><span data-stu-id="6543a-743">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="6543a-744">[重大變更] 已為 'New-AzFirewallPolicyApplicationRule' 和 'New-AzFirewallPolicyNetworkRule' 新增必要參數 'SourceIpGroup'。</span><span class="sxs-lookup"><span data-stu-id="6543a-744">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="6543a-745">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="6543a-745">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="6543a-746">[重大變更] 已修正 'New-AzFirewallPolicyApplicationRule'，參數 'SourceAddress' 會是必要的。</span><span class="sxs-lookup"><span data-stu-id="6543a-746">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="6543a-747">[重大變更] 已移除必要參數：'New-AzFirewallPolicyNatRuleCollection' 的 'TranslatedAddress'、'TranslatedPort'。</span><span class="sxs-lookup"><span data-stu-id="6543a-747">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="6543a-748">已新增 Cmdlet 以在應用程式閘道上支援 PrivateLink</span><span class="sxs-lookup"><span data-stu-id="6543a-748">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="6543a-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-749">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6543a-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-750">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6543a-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-751">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6543a-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-752">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6543a-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-753">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="6543a-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-754">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="6543a-755">已為 VirtualHub 的 HubRouteTables 子資源新增了 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-755">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="6543a-756">'New-AzVHubRoute'</span><span class="sxs-lookup"><span data-stu-id="6543a-756">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="6543a-757">'New-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-757">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6543a-758">'Get-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-758">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6543a-759">'Update-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-759">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="6543a-760">'Remove-AzVHubRouteTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-760">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="6543a-761">已更新現有的 Cmdlet，以支援 VirtualWan 中自訂路由的選擇性 RoutingConfiguration 輸入參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-761">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="6543a-762">'New-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-762">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="6543a-763">'Set-AzExpressRouteConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-763">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="6543a-764">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-764">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6543a-765">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-765">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6543a-766">'New-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-766">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="6543a-767">'Update-AzVpnConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-767">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="6543a-768">'New-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-768">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="6543a-769">'Update-AzP2sVpnGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-769">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-770">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-770">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-771">已修正 PSWorkspace 未實作 IOperationalInsightsWorkspace 的錯誤 (bug) [#12135]</span><span class="sxs-lookup"><span data-stu-id="6543a-771">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="6543a-772">已將 'pergb2018' 新增至 'Set-AzOperationalInsightsWorkspace' 中參數 'Sku' 的有效值集</span><span class="sxs-lookup"><span data-stu-id="6543a-772">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="6543a-773">已將參數 'FunctionParameter' 的別名 'FunctionParameters' 新增至</span><span class="sxs-lookup"><span data-stu-id="6543a-773">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="6543a-774">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6543a-774">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="6543a-775">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6543a-775">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-776">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-777">Azure 備份新增了提取 MAB 項目的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-777">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="6543a-778">Azure Site Recovery 支援磁碟類型 'StandardSSD_LRS'</span><span class="sxs-lookup"><span data-stu-id="6543a-778">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-779">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-779">Az.Resources</span></span>
* <span data-ttu-id="6543a-780">已在 'PSADUser' 上新增 'UsageLocation'、'GivenName'、'Surname'、'AccountEnabled'、'MailNickname'、'Mail' [#10526] [#10497]</span><span class="sxs-lookup"><span data-stu-id="6543a-780">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="6543a-781">已修正 '-Mail' 在 'Get-AzADUser' 上無法運作的問題 [#11981]</span><span class="sxs-lookup"><span data-stu-id="6543a-781">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="6543a-782">已將 '-ExcludeChangeType' 參數新增至 'Get-AzDeploymentWhatIfResult' 和 'Get-AzResourceGroupDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="6543a-782">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="6543a-783">已將 '-WhatIfExcludeChangeType' 參數新增至 'New-AzDeployment' 和 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-783">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="6543a-784">已更新 'Test-Az\*Deployment' Cmdlet，以顯示更好的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-784">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="6543a-785">已針對 deployment create 和 What-If Cmdlet 的 '-Name ' 參數修正說明訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-785">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-786">Az.Sql</span></span>
* <span data-ttu-id="6543a-787">已針對 Set SQL Server Azure Active Directory Admin Cmdlet 新增主體的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-787">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="6543a-788">已修正資料分類 Cmdlet 中的同步處理問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-788">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="6543a-789">支援在 'Set-AzSqlServerActiveDirectoryAdministrator' 上依照郵件搜尋使用者 [#12192]</span><span class="sxs-lookup"><span data-stu-id="6543a-789">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-790">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-790">Az.Storage</span></span>
* <span data-ttu-id="6543a-791">支援使用 RequireInfrastructureEncryption 建立儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-791">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="6543a-792">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-792">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-793">已將載入 Azure.Core 的邏輯移至 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-793">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-794">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-794">Az.Websites</span></span>
* <span data-ttu-id="6543a-795">已新增保護來刪除已建立的 Web 應用程式 (如果還原在 'Restore-AzDeletedWebApp' 中失敗)</span><span class="sxs-lookup"><span data-stu-id="6543a-795">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6543a-796">已為 'New-AzWebApp' 和 'New-AzWebAppSlot' 新增 'SourceWebApp.Location'</span><span class="sxs-lookup"><span data-stu-id="6543a-796">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="6543a-797">已修正無法在 'Set-AzWebApp' 和 'Set-AzWebAppSlot' 中變更容器設定的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-797">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="6543a-798">已修正未提供 Get-AzWebApp 的 -Name 時取得 SiteConfig 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-798">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="6543a-799">已新增為 Linux 應用程式建立 ASP 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-799">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="6543a-800">已在資源群組中新增複製的例外狀況</span><span class="sxs-lookup"><span data-stu-id="6543a-800">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="6543a-801">4.2.0 - 2020 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6543a-801">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-802">Az.Accounts</span></span>
* <span data-ttu-id="6543a-803">已修正可能導致 Az 略過 Azure 自動化或 PowerShell 作業中記錄的問題 [#11492]</span><span class="sxs-lookup"><span data-stu-id="6543a-803">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-804">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-804">Az.AnalysisServices</span></span>
* <span data-ttu-id="6543a-805">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-805">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-806">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-806">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-807">已更新服務管理 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-807">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="6543a-808">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6543a-808">Az.Billing</span></span>
* <span data-ttu-id="6543a-809">已更新耗用量 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-809">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-810">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-810">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-811">支援 PrivateEndpoint 和 PublicNetworkAccess 控制項。</span><span class="sxs-lookup"><span data-stu-id="6543a-811">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-812">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-813">已更新資料處理站 V2 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-813">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="6543a-814">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="6543a-814">Az.DataShare</span></span>
* <span data-ttu-id="6543a-815">''Az.DataShare'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="6543a-815">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="6543a-816">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="6543a-816">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="6543a-817">''Az.DesktopVirtualization'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="6543a-817">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-818">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-818">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-819">已將 SDK 升級至 0.21.0</span><span class="sxs-lookup"><span data-stu-id="6543a-819">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="6543a-820">已將選用參數新增至</span><span class="sxs-lookup"><span data-stu-id="6543a-820">Added optional parameters to</span></span> 
    - <span data-ttu-id="6543a-821">'New-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6543a-821">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="6543a-822">'Set-AzOperationalInsightsSavedSearch'</span><span class="sxs-lookup"><span data-stu-id="6543a-822">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-823">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-823">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-824">已更正 'Start-AzPolicyComplianceScan' 的範例 3</span><span class="sxs-lookup"><span data-stu-id="6543a-824">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6543a-825">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6543a-825">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6543a-826">已更新 PowerBI Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-826">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6543a-827">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6543a-827">Az.PrivateDns</span></span>
* <span data-ttu-id="6543a-828">已更正 Remove-AzPrivateDnsRecordSet 的詳細資訊輸出字串格式</span><span class="sxs-lookup"><span data-stu-id="6543a-828">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-829">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-829">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-830">Azure Site Recovery 支援建立復原計畫，以從 xml 輸入區域到區域複寫。</span><span class="sxs-lookup"><span data-stu-id="6543a-830">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="6543a-831">已更新 SiteRecovery 和備份 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-831">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-832">Az.Resources</span></span>
* <span data-ttu-id="6543a-833">已將 Tail 參數新增至 Get-AzDeploymentScriptLog 和 Save-AzDeploymentScriptLog Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-833">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="6543a-834">已格式化輸出屬性，並將其顯示在 Get-AzDeploymentScript Cmdlet 輸出上</span><span class="sxs-lookup"><span data-stu-id="6543a-834">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="6543a-835">已將 -DeploymentScriptInputObject parameter 參數重新命名為 -DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="6543a-835">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="6543a-836">已修正 Cmdlet 訊息中遺漏的檔案/目標名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-836">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="6543a-837">已更新資源管理員和標記 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-837">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-838">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-838">Az.Sql</span></span>
* <span data-ttu-id="6543a-839">已將 UsePrivateLinkConnection 新增至 'New-AzSqlSyncGroup'、'Update-AzSqlSyncGroup'、'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="6543a-839">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="6543a-840">已將 SyncMemberAzureDatabaseResourceId 新增至 'New-AzSqlSyncMember' 和 'Update-AzSqlSyncMember'</span><span class="sxs-lookup"><span data-stu-id="6543a-840">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="6543a-841">已將來賓使用者查閱支援新增至 Set SQL Server Azure Active Directory Admin Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-841">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-842">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-842">Az.Storage</span></span>
* <span data-ttu-id="6543a-843">已更新資料平面 Cmdlet 的組件版本</span><span class="sxs-lookup"><span data-stu-id="6543a-843">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="6543a-844">4.1.0 - 2020 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6543a-844">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="6543a-845">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-845">Highlights since the last release</span></span>
* <span data-ttu-id="6543a-846">支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="6543a-846">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="6543a-847">Az.Functions 正式發行</span><span class="sxs-lookup"><span data-stu-id="6543a-847">General availability of Az.Functions</span></span> 
* <span data-ttu-id="6543a-848">Az.ApiManagement、Az.Batch、Az.Compute、Az.KeyVault、Az.Monitor、Az.Network、Az.OperationalInsights、Az.Resources 和 Az.Storage 具有主要版本</span><span class="sxs-lookup"><span data-stu-id="6543a-848">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-849">Az.Accounts</span></span>
* <span data-ttu-id="6543a-850">已更新 'Add-AzEnvironment' 和 'Set-AzEnvironment' 以接受 'AzureSynapseAnalyticsEndpointResourceId' 和 'AzureSynapseAnalyticsEndpointSuffix' 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-850">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="6543a-851">已將 Azure.Core 相關組件新增至 Az.Accounts，支援的 PowerShell 平台包括 Windows PowerShell 5.1、PowerShell Core 6.2.4、PowerShell 7+</span><span class="sxs-lookup"><span data-stu-id="6543a-851">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-852">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-852">Az.Aks</span></span>
* <span data-ttu-id="6543a-853">已將 API 版本升級至 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="6543a-853">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="6543a-854">支援使用 Windows 容器建立 AKS</span><span class="sxs-lookup"><span data-stu-id="6543a-854">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="6543a-855">已提供新的 Cmdlet：'New-AzAksNodePool'、'Update-AzAksNodePool'、'Remove-AzAksNodePool'、        'Get-AzAksNodePool'、'Install-AzAksKubectl'、'Get-AzAksVersion'</span><span class="sxs-lookup"><span data-stu-id="6543a-855">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-856">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-856">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-857">'New-AzApiManagement' 與 'Set-AzApiManagement': [-AssignIdentity] 參數已重新命名為 [-SystemAssignedIdentity]</span><span class="sxs-lookup"><span data-stu-id="6543a-857">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="6543a-858">'New-AzApiManagement' 與 'Set-AzApiManagement'：已新增下列參數：[-UserAssignedIdentity <String[]>]</span><span class="sxs-lookup"><span data-stu-id="6543a-858">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="6543a-859">'Get-AzApiManagementProperty'：已重新命名為 'Get-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="6543a-859">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6543a-860">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="6543a-860">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6543a-861">'New-AzApiManagementProperty'：已重新命名為 'New-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="6543a-861">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6543a-862">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="6543a-862">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="6543a-863">'Set-AzApiManagementProperty'：已重新命名為 'Set-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="6543a-863">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6543a-864">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="6543a-864">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6543a-865">'Remove-AzApiManagementProperty'：已重新命名為 'Remove-AzApiManagementNamedValue'。</span><span class="sxs-lookup"><span data-stu-id="6543a-865">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="6543a-866">PropertyId 參數已重新命名為 NamedValueId。</span><span class="sxs-lookup"><span data-stu-id="6543a-866">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="6543a-867">新增的 'Get-AzApiManagementAuthorizationServerClientSecret' Cmdlet 和 'Get-AzApiManagementAuthorizationServer' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="6543a-867">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="6543a-868">新增的 'AzApiManagementNamedValueSecretValue' Cmdlet 和 'AzApiManagementNamedValue' 將不會傳回密碼值。</span><span class="sxs-lookup"><span data-stu-id="6543a-868">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="6543a-869">新增的 'Get-AzApiManagementOpenIdConnectProviderClientSecret' Cmdlet 和 'Get-AzApiManagementOpenIdConnectProvider' 將不再傳回用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="6543a-869">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="6543a-870">新增的 'AzApiManagementSubscriptionKey' Cmdlet 和 'AzApiManagementSubscription' 將不再傳回訂用帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="6543a-870">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="6543a-871">新增的 'AzApiManagementTenantAccessSecret' Cmdlet 和 'AzApiManagementTenantAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="6543a-871">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="6543a-872">新增的 'AzApiManagementTenantGitAccessSecret' Cmdlet 和 'AzApiManagementTenantGitAccess' 將不再傳回金鑰。</span><span class="sxs-lookup"><span data-stu-id="6543a-872">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6543a-873">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-873">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6543a-874">新增的參數：適用於 'New-AzApplicationInsights' 的 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery'</span><span class="sxs-lookup"><span data-stu-id="6543a-874">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="6543a-875">已建立 Cmdlet 'Update-AzApplicationInsights'</span><span class="sxs-lookup"><span data-stu-id="6543a-875">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="6543a-876">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-876">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-877">Az.Batch</span></span>
* <span data-ttu-id="6543a-878">已將 Az.Batch 更新為使用 'Microsoft.Azure.Batch' SDK 版本 13.0.0 和 'Microsoft.Azure.Management.Batch' SDK 版本 9.0.0。</span><span class="sxs-lookup"><span data-stu-id="6543a-878">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="6543a-879">已新增下列功能：使用新的 '-CertificateKind' 參數選取要新增至 'New-AzBatchCertificate' 的憑證種類。</span><span class="sxs-lookup"><span data-stu-id="6543a-879">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="6543a-880">已從 'PSApplication' 中移除先前一律為 '' 的 'ApplicationPackages' 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-880">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="6543a-881">現在可以使用 'Get-AzBatchApplicationPackage' 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="6543a-881">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="6543a-882">例如：'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'。</span><span class="sxs-lookup"><span data-stu-id="6543a-882">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="6543a-883">使用 'New-AzBatchPool' 建立集區時，'PSImageReference' 的 'VirtualMachineImageId' 屬性現在只能參考共用映像庫映像。</span><span class="sxs-lookup"><span data-stu-id="6543a-883">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="6543a-884">使用 'New-AzBatchPool' 建立集區時，可以使用 'PSNetworkConfiguration' 的新 'PublicIPAddressConfiguration' 屬性來佈建集區，無需公用 IP。</span><span class="sxs-lookup"><span data-stu-id="6543a-884">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="6543a-885">'PSNetworkConfiguration' 的 'PublicIPs' 屬性也已移至 'PSPublicIPAddressConfiguration'。</span><span class="sxs-lookup"><span data-stu-id="6543a-885">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="6543a-886">只有當 'IPAddressProvisioningType' 是 'UserManaged' 時，才能指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-886">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-887">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-887">Az.Compute</span></span>
* <span data-ttu-id="6543a-888">已將 HostId 參數新增至 'Update-AzVM' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-888">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="6543a-889">已更新 'New-AzVMConfig'、'New-AzVmssConfig', 'Update-AzVmss'、'Set-AzVMOperatingSystem' 和 'Set-AzVmssOsProfile' Cmdlet 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="6543a-889">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="6543a-890">重大變更</span><span class="sxs-lookup"><span data-stu-id="6543a-890">Breaking changes</span></span>
    - <span data-ttu-id="6543a-891">已從 'Get-AzVMImage' Cmdlet 中移除 FilterExpression 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-891">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="6543a-892">已從 'New-AzVmssConfig'、'New-AzVMConfig' 和 'Update-AzVM' Cmdlet 中移除 AssignIdentity 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-892">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="6543a-893">已從 'New-AzVmssConfig' 和 'Update-AzVmss' Cmdlet 中移除 AutomaticRepairMaxInstanceRepairsPercent。</span><span class="sxs-lookup"><span data-stu-id="6543a-893">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="6543a-894">已從 ProximityPlacementGroup 中移除 AvailabilitySetsColocationStatus、VirtualMachinesColocationStatus 和 VirtualMachineScaleSetsColocationStatus。</span><span class="sxs-lookup"><span data-stu-id="6543a-894">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="6543a-895">已從 AutomaticRepairsPolicy 中移除 MaxInstanceRepairsPercent 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-895">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="6543a-896">AvailabilitySets、VirtualMachines 和 VirtualMachineScaleSets 的類型已從 IList<SubResource> 變更為 IList<SubResourceWithColocationStatus>。</span><span class="sxs-lookup"><span data-stu-id="6543a-896">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="6543a-897">已更新 ' Update-azvm ' Cmdlet 的描述，以提供更好的描述。</span><span class="sxs-lookup"><span data-stu-id="6543a-897">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-898">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-898">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-899">支援受控 IR 中資料流程執行階段屬性的 CRUD。</span><span class="sxs-lookup"><span data-stu-id="6543a-899">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-900">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-900">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-901">已新增用於建立、更新、取出及刪除 Front Door 規則引擎物件的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-901">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="6543a-902">已新增用於建構 Front Door 規則引擎物件的協助程式 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-902">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="6543a-903">已將規則引擎參考新增至 Front Door 路由規則物件。</span><span class="sxs-lookup"><span data-stu-id="6543a-903">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="6543a-904">已將私人連結參數新增至 Front Door 後端物件</span><span class="sxs-lookup"><span data-stu-id="6543a-904">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="6543a-905">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="6543a-905">Az.Functions</span></span>
* <span data-ttu-id="6543a-906">''Az.Functions'' 模組正式發行</span><span class="sxs-lookup"><span data-stu-id="6543a-906">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-907">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-907">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-908">支援客戶管理的金鑰磁碟加密。</span><span class="sxs-lookup"><span data-stu-id="6543a-908">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6543a-909">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6543a-909">Az.HealthcareApis</span></span>
* <span data-ttu-id="6543a-910">存取原則不再預設為目前的主體</span><span class="sxs-lookup"><span data-stu-id="6543a-910">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-911">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-911">Az.IotHub</span></span>
* <span data-ttu-id="6543a-912">已新增 Cmdlet 來叫用 IoT 中樞內的查詢，以使用類似 SQL 的語言來取出資訊。</span><span class="sxs-lookup"><span data-stu-id="6543a-912">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="6543a-913">已修正下列問題：沒有子裝置，'Add-AzIotHubDevice' 無法建立已啟用 Edge 的裝置 [#11597]</span><span class="sxs-lookup"><span data-stu-id="6543a-913">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="6543a-914">已新增 Cmdlet 來產生 Iot 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="6543a-914">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="6543a-915">已新增 Cmdlet 來叫用設定計量查詢。</span><span class="sxs-lookup"><span data-stu-id="6543a-915">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="6543a-916">管理大規模的 IoT Edge 自動部署。</span><span class="sxs-lookup"><span data-stu-id="6543a-916">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="6543a-917">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-917">New cmdlets are:</span></span>
    - <span data-ttu-id="6543a-918">'Add-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-918">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6543a-919">'Get-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-919">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6543a-920">'Remove-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-920">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="6543a-921">'Set-AzIotHubDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-921">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="6543a-922">已新增 Cmdlet 來叫用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="6543a-922">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="6543a-923">已新增 Cmdlet 將設定內容套用至指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="6543a-923">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-924">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-924">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-925">已移除兩個別名：'New-AzKeyVaultCertificateAdministratorDetails' 和 'New-AzKeyVaultCertificateOrganizationDetails'</span><span class="sxs-lookup"><span data-stu-id="6543a-925">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="6543a-926">建立金鑰保存庫時，依預設會啟用虛刪除</span><span class="sxs-lookup"><span data-stu-id="6543a-926">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="6543a-927">在建立金鑰保存庫時，可以設定網路規則，以管理來自特定網路位置的協助工具</span><span class="sxs-lookup"><span data-stu-id="6543a-927">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="6543a-928">已新增攜帶您自己的金鑰 (BYOK) 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-928">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="6543a-929">'Add-AzKeyVaultKey' 支援產生金鑰交換金鑰</span><span class="sxs-lookup"><span data-stu-id="6543a-929">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="6543a-930">'Get-AzKeyVaultKey' 支援以 PEM 格式下載公開金鑰</span><span class="sxs-lookup"><span data-stu-id="6543a-930">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="6543a-931">已更新 'Add-AzKeyVaultKey' 說明文件的 'KeyOps' 部分</span><span class="sxs-lookup"><span data-stu-id="6543a-931">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-932">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-932">Az.Monitor</span></span>
* <span data-ttu-id="6543a-933">已修正 'AzDiagnosticSettings' 的下列錯誤 (bug)：保留原則不會套用到所有類別 [#11589]</span><span class="sxs-lookup"><span data-stu-id="6543a-933">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="6543a-934">計量警示 V2 支援 WebTest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="6543a-934">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="6543a-935">'New-AzMetricAlertRuleV2Criteria'：已新增建立 webtest 可用性準則的選項</span><span class="sxs-lookup"><span data-stu-id="6543a-935">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="6543a-936">'Add-AzMetricAlertRuleV2'：支援新的 webtest 可用性準則</span><span class="sxs-lookup"><span data-stu-id="6543a-936">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="6543a-937">已移除 PSLogProfile 中 RetentionPolicy 的備援定義 [#7608]</span><span class="sxs-lookup"><span data-stu-id="6543a-937">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="6543a-938">已移除 PSEventData 中定義的備援屬性 [#11353]</span><span class="sxs-lookup"><span data-stu-id="6543a-938">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="6543a-939">已將 'Get-AzLog' 重新命名為 'Get-AzActivityLog'</span><span class="sxs-lookup"><span data-stu-id="6543a-939">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-940">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-940">Az.Network</span></span>
* <span data-ttu-id="6543a-941">已新增重大變更屬性，以通知區域預設行為將會變更</span><span class="sxs-lookup"><span data-stu-id="6543a-941">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="6543a-942">'New-AzPublicIpAddress'</span><span class="sxs-lookup"><span data-stu-id="6543a-942">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="6543a-943">'New-AzPublicIpPrefix'</span><span class="sxs-lookup"><span data-stu-id="6543a-943">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="6543a-944">'New-AzLoadBalancerFrontendIpConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-944">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="6543a-945">已新增最上層資源 SecurityPartnerProvider 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-945">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="6543a-946">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-946">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-947">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6543a-947">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6543a-948">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6543a-948">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6543a-949">Get-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6543a-949">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="6543a-950">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="6543a-950">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="6543a-951">已在 'PSPrivateLinkResource' 上新增 'RequiredZoneNames'，並在 'PSPrivateEndpointConnection' 上新增 'GroupId'</span><span class="sxs-lookup"><span data-stu-id="6543a-951">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="6543a-952">已針對 New-AzNetworkWatcherConnectionMonitorTestConfigurationObject 修正 SuccessThresholdRoundTripTimeMs 參數的不正確類型</span><span class="sxs-lookup"><span data-stu-id="6543a-952">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="6543a-953">已更新 VirtualWan Cmdlet，將 AllowVnetToVnetTraffic 引數的預設值設為 True。</span><span class="sxs-lookup"><span data-stu-id="6543a-953">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="6543a-954">'New-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="6543a-954">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="6543a-955">'Update-AzVirtualWan'</span><span class="sxs-lookup"><span data-stu-id="6543a-955">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="6543a-956">已新增 Cmdlet 來支援私人端點的 DNS 區域群組</span><span class="sxs-lookup"><span data-stu-id="6543a-956">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="6543a-957">'New-AzPrivateDnsZoneConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-957">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="6543a-958">'Get-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6543a-958">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6543a-959">'New-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6543a-959">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6543a-960">'Set-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6543a-960">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="6543a-961">'Remove-AzPrivateDnsZoneGroup'</span><span class="sxs-lookup"><span data-stu-id="6543a-961">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="6543a-962">已將 'DNSEnableProxy'、'DNSRequireProxyForNetworkRules' 和 'DNSServers' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="6543a-962">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="6543a-963">已將 'EnableDnsProxy'、'DnsProxyNotRequiredForNetworkRule' 和 'DnsServer' 參數新增至 'AzureFirewall'</span><span class="sxs-lookup"><span data-stu-id="6543a-963">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="6543a-964">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-964">Updated cmdlet:</span></span>
        - <span data-ttu-id="6543a-965">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="6543a-965">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-966">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-966">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-967">已更新舊版程式碼以套用新產生的 SDK</span><span class="sxs-lookup"><span data-stu-id="6543a-967">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="6543a-968">由於已取代 API，刪除了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-968">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="6543a-969">'Get-AzOperationalInsightsSavedSearchResult' (別名 'Get-AzOperationalInsightsSavedSearchResults')</span><span class="sxs-lookup"><span data-stu-id="6543a-969">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="6543a-970">'Get-AzOperationalInsightsSearchResult' (別名 'Get-AzOperationalInsightsSearchResults')</span><span class="sxs-lookup"><span data-stu-id="6543a-970">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="6543a-971">'Get-AzOperationalInsightsLinkTarget' (別名 'Get-AzOperationalInsightsLinkTargets')</span><span class="sxs-lookup"><span data-stu-id="6543a-971">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="6543a-972">已新增 'Set-AzOperationalInsightsWorkspace' 和 'New-AzOperationalInsightsWorkspace' 的參數</span><span class="sxs-lookup"><span data-stu-id="6543a-972">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="6543a-973">已針對連結的儲存體帳戶建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-973">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="6543a-974">已針對叢集和連結服務建立 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-974">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-975">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-975">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-976">Azure Site Recovery 已將保護 Azure 鄰近放置群組虛擬機器的支援新增至 Azure 提供者。</span><span class="sxs-lookup"><span data-stu-id="6543a-976">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="6543a-977">Azure Site Recovery 已將區域的支援新增至區域複本。</span><span class="sxs-lookup"><span data-stu-id="6543a-977">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="6543a-978">Azure 備份已新增適用於 Azure FileShare 復原點的長期保留支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-978">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="6543a-979">Azure 備份已將磁片排除屬性新增至 'Get-AzRecoveryServicesBackupItem' Cmdlet 輸出。</span><span class="sxs-lookup"><span data-stu-id="6543a-979">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="6543a-980">已針對站台復原服務新增保存庫認證檔的私人端點。</span><span class="sxs-lookup"><span data-stu-id="6543a-980">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-981">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-981">Az.Resources</span></span>
* <span data-ttu-id="6543a-982">已新增有關在建立新角色定義時檢視延遲的訊息警告</span><span class="sxs-lookup"><span data-stu-id="6543a-982">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="6543a-983">已變更原則 Cmdlet 以輸出強型別物件</span><span class="sxs-lookup"><span data-stu-id="6543a-983">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="6543a-984">已移除用於 'Get-AzResourceLock' Cmdlet 的 '-TenantLevel ' 參數 [#11335]</span><span class="sxs-lookup"><span data-stu-id="6543a-984">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="6543a-985">已修正 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span><span class="sxs-lookup"><span data-stu-id="6543a-985">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="6543a-986">已新增在資源群組範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentResourceGroupWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="6543a-986">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="6543a-987">已新增在訂用帳戶範圍中取得 ARM 範本 What-If 結果的 Cmdlet：'Get-AzDeploymentWhatIfResult'</span><span class="sxs-lookup"><span data-stu-id="6543a-987">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="6543a-988">Alias:'Get-AzSubscriptionDeploymentWhatIf'</span><span class="sxs-lookup"><span data-stu-id="6543a-988">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="6543a-989">已覆寫 'New-AzDeployment' 和 'New-AzResourceGroupDeployment' 的 '-WhatIf' 和 '-Confirm' 參數，以使用 ARM 範本 What-If 結果</span><span class="sxs-lookup"><span data-stu-id="6543a-989">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="6543a-990">已在部署 Cmdlet 中新增 'ApiVersion' 參數的取代訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-990">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="6543a-991">已新增為部署失敗顯示已改善錯誤訊息的功能</span><span class="sxs-lookup"><span data-stu-id="6543a-991">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="6543a-992">已新增針對部署失敗記錄的 correlationId</span><span class="sxs-lookup"><span data-stu-id="6543a-992">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="6543a-993">已將 'error' 屬性新增至部署指令碼輸出</span><span class="sxs-lookup"><span data-stu-id="6543a-993">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="6543a-994">已將 nuget Microsoft.Azure.Management.ResourceManager 更新為 '3.7.1-preview'</span><span class="sxs-lookup"><span data-stu-id="6543a-994">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="6543a-995">當 DeploymentValidateResult 中的 Error 屬性變更為唯讀時，已從 nuget 3.7.1-preview 中移除特定測試案例</span><span class="sxs-lookup"><span data-stu-id="6543a-995">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="6543a-996">已從 SDK ResourceManager 3.7.1-preview 引進 GenericResourceExpanded</span><span class="sxs-lookup"><span data-stu-id="6543a-996">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="6543a-997">已針對用於部署的所有 Get Cmdlet 以及下列 Cmdlet 新增標籤支援：</span><span class="sxs-lookup"><span data-stu-id="6543a-997">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="6543a-998">'New-AzDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-998">'New-AzDeployment'</span></span>
    - <span data-ttu-id="6543a-999">'New-AzManagementGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-999">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="6543a-1000">'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-1000">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6543a-1001">'New-AzTenantDeployment'</span><span class="sxs-lookup"><span data-stu-id="6543a-1001">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-1002">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-1002">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-1003">已修正下列錯誤 (bug)：使用 --SecretIdentifier 新增憑證時取得錯誤憑證指紋</span><span class="sxs-lookup"><span data-stu-id="6543a-1003">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1004">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1004">Az.Sql</span></span>
* <span data-ttu-id="6543a-1005">增強下列項目的效能：</span><span class="sxs-lookup"><span data-stu-id="6543a-1005">Enhance performance of:</span></span>
    - <span data-ttu-id="6543a-1006">'Set-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6543a-1006">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6543a-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6543a-1007">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6543a-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6543a-1008">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6543a-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span><span class="sxs-lookup"><span data-stu-id="6543a-1009">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="6543a-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6543a-1010">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6543a-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6543a-1011">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6543a-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6543a-1012">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="6543a-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span><span class="sxs-lookup"><span data-stu-id="6543a-1013">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="6543a-1014">已從 Cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy' 移除 'RetentionDays' 參數的用戶端驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-1014">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="6543a-1015">在 Vnet 中對儲存體帳戶進行稽核時，修正在建立儲存體 Blob 資料參與者角色時發生的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-1015">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1016">Az.Storage</span></span>
* <span data-ttu-id="6543a-1017">已新增 '-AsJob' 以取得/列出帳戶 Cmdlet 'Get-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1017">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-1018">使用 KeyvaultEncryption 更新儲存體帳戶以支援金鑰自動輪替時，使 KeyVersion 成為選用項目</span><span class="sxs-lookup"><span data-stu-id="6543a-1018">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="6543a-1019">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1019">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-1020">已修正由於管道無法移除 Azure 檔案目錄的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1020">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="6543a-1021">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6543a-1021">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="6543a-1022">已修正 [#9880]：變更 NetWorkRule DefaultAction 值定義以符合 Swagger。</span><span class="sxs-lookup"><span data-stu-id="6543a-1022">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="6543a-1023">'Update-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="6543a-1023">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="6543a-1024">'Get-AzStorageAccountNetworkRuleSet'</span><span class="sxs-lookup"><span data-stu-id="6543a-1024">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="6543a-1025">已修正 [#11624]：新增 NetworkRules 時跳過重複的規則，以避免伺服器失敗</span><span class="sxs-lookup"><span data-stu-id="6543a-1025">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="6543a-1026">'Add-AzStorageAccountNetworkRule'</span><span class="sxs-lookup"><span data-stu-id="6543a-1026">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="6543a-1027">已將 Microsoft.Azure.Cosmos.Table SDK 升級至 1.0.7</span><span class="sxs-lookup"><span data-stu-id="6543a-1027">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="6543a-1028">已新增警告訊息，以在清單 DataLake Gen2 項目中只傳回部分項目時，提醒使用者再次與 ContinuationToken 一起列出</span><span class="sxs-lookup"><span data-stu-id="6543a-1028">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="6543a-1029">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="6543a-1029">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="6543a-1030">已支援使用 Azure Files Active Directory 網域服務驗證來建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1030">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="6543a-1031">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1031">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="6543a-1032">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1032">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-1033">支援新增或列出儲存體帳戶的 Kerberos 金鑰</span><span class="sxs-lookup"><span data-stu-id="6543a-1033">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="6543a-1034">'New-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6543a-1034">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="6543a-1035">'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="6543a-1035">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6543a-1036">支援容錯移轉儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1036">Supported failover Storage account</span></span>
    - <span data-ttu-id="6543a-1037">'Invoke-AzStorageAccountFailover'</span><span class="sxs-lookup"><span data-stu-id="6543a-1037">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="6543a-1038">已更新 'Get-AzStorageBlobCopyState' 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-1038">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="6543a-1039">已更新 'Get-AzStorageFileCopyState' 和 'Start-AzStorageBlobCopy' 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-1039">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="6543a-1040">已將儲存體用戶端程式庫 v12 整合到佇列和檔案 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1040">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="6543a-1041">已將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1041">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6543a-1042">'Get-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="6543a-1042">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="6543a-1043">'Remove-AzStorageFile'</span><span class="sxs-lookup"><span data-stu-id="6543a-1043">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="6543a-1044">'Get-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-1044">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="6543a-1045">'Set-AzStorageFileContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-1045">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="6543a-1046">'Start-AzStorageFileCopy'</span><span class="sxs-lookup"><span data-stu-id="6543a-1046">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="6543a-1047">已將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1047">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6543a-1048">'New-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6543a-1048">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="6543a-1049">'Remove-AzStorageDirectory'</span><span class="sxs-lookup"><span data-stu-id="6543a-1049">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="6543a-1050">已將輸出類型從 CloudFileShare 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1050">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="6543a-1051">'Get-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-1051">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="6543a-1052">'New-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-1052">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="6543a-1053">'Remove-AzStorageShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-1053">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="6543a-1054">已將輸出類型從 FileShareProperties 變更為 AzureStorageFileShare，原始輸出將成為新輸出的子屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1054">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="6543a-1055">'Set-AzStorageShareQuota'</span><span class="sxs-lookup"><span data-stu-id="6543a-1055">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6543a-1056">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6543a-1056">Az.TrafficManager</span></span>
* <span data-ttu-id="6543a-1057">已修正 'DisableAzureTrafficManagerEndpoint' 詳細資訊輸出中不正確的設定檔名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-1057">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1058">Az.Websites</span></span>
* <span data-ttu-id="6543a-1059">已修正 'Update-AzWebAppAccessRestrictionConfig' 說明上的錯字。</span><span class="sxs-lookup"><span data-stu-id="6543a-1059">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="6543a-1060">3.8.0 - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1060">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="6543a-1061">上次發佈版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-1061">Highlights since the last release</span></span>
* <span data-ttu-id="6543a-1062">Az.Storage 支援的 PowerShell 版本：Windows PowerShell 5.1、PowerShell Core 6.2.4+、PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="6543a-1062">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1063">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1063">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1064">更新 'Resolve-AzError' 中的 Azure PowerShell 問卷 URL [#11507]</span><span class="sxs-lookup"><span data-stu-id="6543a-1064">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-1065">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-1065">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-1066">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="6543a-1066">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6543a-1067">'Set-AzApiManagementGroup' 已更新文件以指定 GroupId 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1067">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-1068">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-1068">Az.Cdn</span></span>
* <span data-ttu-id="6543a-1069">已修正 ChinaCDN 相關的定價 SKU 顯示</span><span class="sxs-lookup"><span data-stu-id="6543a-1069">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-1070">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1070">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-1071">支援身分識別、加密、UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="6543a-1071">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1072">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1072">Az.Compute</span></span>
* <span data-ttu-id="6543a-1073">已新增 'Set-AzVmssOrchestrationServiceState' Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1073">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="6543a-1074">具有 -InstanceView 的 'Get-AzVmss' 會顯示 OrchestrationService 狀態。</span><span class="sxs-lookup"><span data-stu-id="6543a-1074">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1075">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1075">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1076">管理 IoT 裝置對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1076">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1077">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6543a-1077">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="6543a-1078">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="6543a-1078">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="6543a-1079">已新增 Cmdlet，可在 IoT 中樞的裝置上叫用直接方法。</span><span class="sxs-lookup"><span data-stu-id="6543a-1079">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="6543a-1080">管理 IoT 裝置模組對應項設定，新的 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1080">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1081">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6543a-1081">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="6543a-1082">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="6543a-1082">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="6543a-1083">大規模管理 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="6543a-1083">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="6543a-1084">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1084">New cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1085">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-1085">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6543a-1086">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-1086">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6543a-1087">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-1087">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="6543a-1088">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="6543a-1088">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="6543a-1089">已新增 Cmdlet，叫用 IoT 中樞的邊緣模組方法。</span><span class="sxs-lookup"><span data-stu-id="6543a-1089">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-1090">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1090">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-1091">已新增可在保存庫上啟用虛刪除和清除保護的新 Cmdlet 'Update-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="6543a-1091">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="6543a-1092">已將支援新增至 Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="6543a-1092">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="6543a-1093">已修正 'Remove-AzKeyVaultManagedStorageSasDefinition' 範例中的錯誤 [#11479]</span><span class="sxs-lookup"><span data-stu-id="6543a-1093">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="6543a-1094">已將支援新增至私人端點</span><span class="sxs-lookup"><span data-stu-id="6543a-1094">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="6543a-1095">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="6543a-1095">Az.Maintenance</span></span>
* <span data-ttu-id="6543a-1096">發行用於 GA 的維護 Cmdlet 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-1096">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1097">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1097">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1098">已新增私人連結範圍的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1098">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="6543a-1099">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6543a-1099">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6543a-1100">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6543a-1100">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6543a-1101">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6543a-1101">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6543a-1102">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="6543a-1102">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="6543a-1103">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6543a-1103">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6543a-1104">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6543a-1104">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="6543a-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="6543a-1105">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1106">Az.Network</span></span>
* <span data-ttu-id="6543a-1107">已更新 Cmdlet，可在私人 IP 上啟用虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="6543a-1107">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="6543a-1108">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-1108">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6543a-1109">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-1109">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="6543a-1110">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-1110">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="6543a-1111">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-1111">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="6543a-1112">已更新 Cmdlet，可啟用以 FQDN 為基礎的 LocalNetworkGateways 和 VpnSites</span><span class="sxs-lookup"><span data-stu-id="6543a-1112">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="6543a-1113">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="6543a-1113">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="6543a-1114">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="6543a-1114">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="6543a-1115">已在 ExpressRouteCircuitConnectionConfig 中新增對 IPv6 位址系列的支援 (全球適用)</span><span class="sxs-lookup"><span data-stu-id="6543a-1115">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="6543a-1116">已新增 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-1116">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6543a-1117">允許設定所有現有屬性，包括 IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="6543a-1117">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="6543a-1118">已更新 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="6543a-1118">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="6543a-1119">已新增另一個選擇性參數 AddressPrefixType 來指定位址首碼的位址系列</span><span class="sxs-lookup"><span data-stu-id="6543a-1119">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="6543a-1120">已更新 Cmdlet，可啟用虛擬網路閘道連線上的 DPD 逾時設定。</span><span class="sxs-lookup"><span data-stu-id="6543a-1120">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="6543a-1121">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1121">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="6543a-1122">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1122">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-1123">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-1123">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-1124">已新增用於觸發原則合規性掃描的 'Start-AzPolicyComplianceScan' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1124">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="6543a-1125">已將原則定義、設定定義和指派版本新增至 'Get-AzPolicyState' 輸出</span><span class="sxs-lookup"><span data-stu-id="6543a-1125">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-1126">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-1126">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-1127">已改善 'New-AzServiceFabricCluster' 範例的程式碼格式設定和可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-1127">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1128">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1128">Az.Sql</span></span>
* <span data-ttu-id="6543a-1129">已新增 'Get-AzSqlInstanceOperation' 和 'Stop-AzSqlInstanceOperation' Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1129">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="6543a-1130">支援對 VNet 中的儲存體帳戶進行稽核。</span><span class="sxs-lookup"><span data-stu-id="6543a-1130">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1131">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1131">Az.Storage</span></span>
* <span data-ttu-id="6543a-1132">在未來版本中新增 Azure 檔案 Cmdlet 輸出變更的重大變更通知</span><span class="sxs-lookup"><span data-stu-id="6543a-1132">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="6543a-1133">建立/更新儲存體帳戶時，支援新的 SkuName StandardGZRS、StandardRAGZRS</span><span class="sxs-lookup"><span data-stu-id="6543a-1133">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="6543a-1134">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1134">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="6543a-1135">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1135">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="6543a-1136">支援 DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="6543a-1136">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="6543a-1137">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-1137">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6543a-1138">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-1138">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6543a-1139">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="6543a-1139">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="6543a-1140">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-1140">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6543a-1141">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="6543a-1141">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="6543a-1142">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-1142">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="6543a-1143">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="6543a-1143">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="6543a-1144">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="6543a-1144">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="6543a-1145">0.10.0-preview - 2020 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1145">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="6543a-1146">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-1146">General</span></span>
* <span data-ttu-id="6543a-1147">Az 模組現已在 Azure Stack Hub 中提供預覽。</span><span class="sxs-lookup"><span data-stu-id="6543a-1147">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="6543a-1148">此模組具有 Linux 和 macOs 的跨平台相容性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1148">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="6543a-1149">Azure Stack Hub 現在支援使用 Az 模組的 PowerShell Core，如需詳細資訊，請參閱[這裡](https://aka.ms/az4AzureStack)</span><span class="sxs-lookup"><span data-stu-id="6543a-1149">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="6543a-1150">Az 模組支援 2019-03-01-hybrid 設定檔：</span><span class="sxs-lookup"><span data-stu-id="6543a-1150">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="6543a-1151">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6543a-1151">Az.Billing</span></span>
  - <span data-ttu-id="6543a-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1152">Az.Compute</span></span>
  - <span data-ttu-id="6543a-1153">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6543a-1153">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="6543a-1154">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1154">Az.EventHub</span></span>
  - <span data-ttu-id="6543a-1155">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1155">Az.IotHub</span></span>
  - <span data-ttu-id="6543a-1156">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1156">Az.KeyVault</span></span>
  - <span data-ttu-id="6543a-1157">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1157">Az.Monitor</span></span>
  - <span data-ttu-id="6543a-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1158">Az.Network</span></span>
  - <span data-ttu-id="6543a-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1159">Az.Resources</span></span>
  - <span data-ttu-id="6543a-1160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1160">Az.Storage</span></span>
  - <span data-ttu-id="6543a-1161">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1161">Az.Websites</span></span>
* <span data-ttu-id="6543a-1162">已引進三個可搭配 Azure Stack Hub 且適用於 az 的新 PowerShell 模組，包括 Az.Databox、Az.IotHub 和 Az. EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1162">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="6543a-1163">命令維持不變，但有次要變更，例如將 AzureRM 變更為 Az</span><span class="sxs-lookup"><span data-stu-id="6543a-1163">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="6543a-1164">您可以在[這裡](https://aka.ms/InstallASHPowerShell)找到 Azure Stack Hub 的 PowerShell 文件更新連結</span><span class="sxs-lookup"><span data-stu-id="6543a-1164">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="6543a-1165">3.7.0 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1165">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-1166">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1166">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1167">已修正 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' 在未登入時擲回 NullReferenceException [#10292]</span><span class="sxs-lookup"><span data-stu-id="6543a-1167">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1168">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1168">Az.Compute</span></span>
* <span data-ttu-id="6543a-1169">已將下列參數新增至 'New-AzDiskConfig' Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1169">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="6543a-1170">DiskIOPSReadOnly、DiskMBpsReadOnly、MaxSharesCount、GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="6543a-1170">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="6543a-1171">允許 'New-AzGalleryImageVersion' Cmdlet 目標參數的加密屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1171">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="6543a-1172">已修正 'Set-AzVmss' -Reimage 和 'Invoke-AzVMReimage' Cmdlet 的 tempDisk 問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1172">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="6543a-1173">[#11354]</span><span class="sxs-lookup"><span data-stu-id="6543a-1173">[#11354]</span></span>
* <span data-ttu-id="6543a-1174">已針對新的 SAP 延伸模組，將支援新增至下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1174">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="6543a-1175">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-1175">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6543a-1176">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-1176">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6543a-1177">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-1177">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="6543a-1178">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="6543a-1178">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="6543a-1179">已修正說明文件範例中的錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-1179">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="6543a-1180">以表格格式顯示 VM PowerState 的確切字串值。</span><span class="sxs-lookup"><span data-stu-id="6543a-1180">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="6543a-1181">'New-AzVmssConfig'：已修正當 SinglePlacementGroup 停用時 AutomaticRepairs 屬性的序列化。</span><span class="sxs-lookup"><span data-stu-id="6543a-1181">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="6543a-1182">[#11257]</span><span class="sxs-lookup"><span data-stu-id="6543a-1182">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1183">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1183">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1184">已將 ADF .Net SDK 版本更新為 4.8.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1184">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="6543a-1185">已將選擇性參數新增至 'Invoke-AzDataFactoryV2Pipeline' 命令以支援重新執行</span><span class="sxs-lookup"><span data-stu-id="6543a-1185">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-1186">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-1186">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-1187">已新增 'Export-AzDataLakeStoreItem' 和 'Import-AzDataLakeStoreItem' 的中斷性變更描述</span><span class="sxs-lookup"><span data-stu-id="6543a-1187">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="6543a-1188">已新增 'New-AzDataLakeStoreItem'、'Add-AzDAtaLakeStoreItemContent' 和 'Get-AzDAtaLakeStoreItemContent' 的位元組編碼選項</span><span class="sxs-lookup"><span data-stu-id="6543a-1188">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-1189">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-1189">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-1190">支援在建立叢集時指定支援的最低 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="6543a-1190">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1191">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1191">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1192">已新增管理每一部裝置的分散式設定支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1192">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="6543a-1193">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1193">New Cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1194">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6543a-1194">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="6543a-1195">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="6543a-1195">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-1196">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1196">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-1197">已將中斷性變更屬性新增至 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="6543a-1197">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1198">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1198">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1199">已更新 'New-AzScheduledQueryRuleLogMetricTrigger' 的文件</span><span class="sxs-lookup"><span data-stu-id="6543a-1199">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1200">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1200">Az.Network</span></span>
* <span data-ttu-id="6543a-1201">已更新 Cmdlet 以允許跨租用戶 VirtualHubVnetConnections</span><span class="sxs-lookup"><span data-stu-id="6543a-1201">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="6543a-1202">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-1202">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6543a-1203">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="6543a-1203">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="6543a-1204">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6543a-1204">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="6543a-1205">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="6543a-1205">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="6543a-1206">已移除 SQL 管理 SDK 相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-1206">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-1207">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-1207">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-1208">改善錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-1208">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1209">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1209">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1210">Azure Site Recovery 已新增重新保護的支援，並且已更新 Azure 磁碟加密虛擬機器的 VM 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1210">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="6543a-1211">已新增 Azure Site Recovery VmwareToAzure 屬性 DR 監視</span><span class="sxs-lookup"><span data-stu-id="6543a-1211">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="6543a-1212">Azure 備份已新增針對失敗項目重試原則更新的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1212">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="6543a-1213">Azure 備份已新增在備份和還原期間對磁碟排除設定的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1213">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="6543a-1214">Azure 備份已新增在 AzureFileShare 中還原多個檔案/資料夾的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1214">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="6543a-1215">Azure 備份已新增在更新 IaasVM 原則時對使用者指定 Resourcegroup 支援的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1215">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1216">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1216">Az.Resources</span></span>
* <span data-ttu-id="6543a-1217">已修正 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' 以使用實際的資源 apiVersion，而不是預設 apiVersion [#11267]</span><span class="sxs-lookup"><span data-stu-id="6543a-1217">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="6543a-1218">已新增對於錯誤案例的 correlationId 記錄</span><span class="sxs-lookup"><span data-stu-id="6543a-1218">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="6543a-1219">小型文件變更為 'Get-AzResourceLock'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1219">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="6543a-1220">已新增範例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1220">Added example.</span></span>
* <span data-ttu-id="6543a-1221">已逸出 'Get-AzADUser' 參數值中的單引號 [#11317]</span><span class="sxs-lookup"><span data-stu-id="6543a-1221">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="6543a-1222">已新增部署指令碼 ('Get-AzDeploymentScript'、'Get-AzDeploymentScriptLog'、'Save-AzDeploymentScriptLog'、'Remove-AzDeploymentScript') 的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1222">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1223">Az.Sql</span></span>
* <span data-ttu-id="6543a-1224">已將可讀取次要參數新增至 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="6543a-1224">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="6543a-1225">已新增 Cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="6543a-1225">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="6543a-1226">已儲存在資料庫中分類資料行時的敏感度等級。</span><span class="sxs-lookup"><span data-stu-id="6543a-1226">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="6543a-1227">Az.Support</span><span class="sxs-lookup"><span data-stu-id="6543a-1227">Az.Support</span></span>
* <span data-ttu-id="6543a-1228">'Az.Support' 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-1228">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1229">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1229">Az.Websites</span></span>
* <span data-ttu-id="6543a-1230">已透過以下新 Cmdlet 新增使用 webapp 流量路由規則的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1230">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="6543a-1231">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6543a-1231">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6543a-1232">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6543a-1232">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6543a-1233">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6543a-1233">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="6543a-1234">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="6543a-1234">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="6543a-1235">3.6.1 - 2020 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1235">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-1236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1236">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1237">在 'Send-Feedback' 中開啟 Azure PowerShell 問卷頁面 [#11020]</span><span class="sxs-lookup"><span data-stu-id="6543a-1237">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="6543a-1238">在 'Resolve-Error' 中顯示 Azure PowerShell 問卷 URL [#11021]</span><span class="sxs-lookup"><span data-stu-id="6543a-1238">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="6543a-1239">已在 UserAgent 中新增 Az 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-1239">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-1240">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-1240">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-1241">已新增可在 DeveloperPortal 端點上擷取和設定自訂網域的支援 [#11007]</span><span class="sxs-lookup"><span data-stu-id="6543a-1241">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="6543a-1242">'Export-AzApiManagementApi' 已新增以 JSON 格式下載 API 定義的支援 [#9987]</span><span class="sxs-lookup"><span data-stu-id="6543a-1242">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="6543a-1243">'Import-AzApiManagementApi' 已新增從 JSON 文件匯入 OpenAPI 3.0 定義的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1243">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="6543a-1244">'New-AzApiManagementIdentityProvider' 和 'Set-AzApiManagementIdentityProvider' 已新增為 AAD B2C 提供者設定「登入租用戶」的支援 [#9784]</span><span class="sxs-lookup"><span data-stu-id="6543a-1244">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-1245">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-1245">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-1246">已在 csproj 和 psd1 中明確新增對 System.Buffers 的參考。</span><span class="sxs-lookup"><span data-stu-id="6543a-1246">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1247">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1247">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1248">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1248">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6543a-1249">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1249">New Cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1250">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1250">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1251">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1251">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1252">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1252">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1253">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1253">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="6543a-1254">已新增可在 Iot 中樞的目標 Iot 裝置上管理模組的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1254">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="6543a-1255">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1255">New Cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1256">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6543a-1256">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="6543a-1257">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6543a-1257">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="6543a-1258">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6543a-1258">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="6543a-1259">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="6543a-1259">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="6543a-1260">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置的連接字串。</span><span class="sxs-lookup"><span data-stu-id="6543a-1260">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6543a-1261">已新增 Cmdlet，以取得 Iot 中樞內目標 IoT 裝置上的模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="6543a-1261">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="6543a-1262">已新增可取得/設定 IoT 裝置父系裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1262">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="6543a-1263">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1263">New Cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1264">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6543a-1264">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="6543a-1265">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="6543a-1265">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="6543a-1266">已新增可管理裝置父子關聯性的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1266">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1267">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1267">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1268">已修正 'Get-AzMetricDefinition' 的輸出值 [#9714]</span><span class="sxs-lookup"><span data-stu-id="6543a-1268">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1269">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1269">Az.Network</span></span>
* <span data-ttu-id="6543a-1270">已更新 Sql Management SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-1270">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="6543a-1271">已修正 PrivateLinkServiceConnectionState 類別中的命名差異問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1271">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="6543a-1272">將欄位 ActionsRequired 對應至 ActionRequired。</span><span class="sxs-lookup"><span data-stu-id="6543a-1272">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="6543a-1273">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1273">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1274">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1274">Az.Resources</span></span>
* <span data-ttu-id="6543a-1275">已修正 'Get-AzRoleAssignment' 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-1275">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="6543a-1276">已將 'Remove-AzADGroup' 中的 '-Force' 和 '-PassThru' 參數標記為選擇性 [#10849]</span><span class="sxs-lookup"><span data-stu-id="6543a-1276">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="6543a-1277">已修正 'MailNickname' 不會在 'Remove-AzADGroup' 中傳回的問題 [#11167]</span><span class="sxs-lookup"><span data-stu-id="6543a-1277">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="6543a-1278">已修正 'Remove-AzADGroup' 管道作業無法運作的問題 [#11171]</span><span class="sxs-lookup"><span data-stu-id="6543a-1278">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="6543a-1279">已修正 GetAzureRoleAssignmentCommand 中的 Null 參考錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-1279">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="6543a-1280">已針對原則 Cmdlet 即將來臨的變更新增重大變更屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1280">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="6543a-1281">已更新 'Get-AzResourceGroup' 以在伺服器端執行資源群組標籤篩選</span><span class="sxs-lookup"><span data-stu-id="6543a-1281">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="6543a-1282">已擴充標籤 Cmdlet 以接受 -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6543a-1282">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="6543a-1283">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6543a-1283">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6543a-1284">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6543a-1284">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="6543a-1285">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6543a-1285">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="6543a-1286">已新增標籤 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1286">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="6543a-1287">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="6543a-1287">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="6543a-1288">從 SDK 3.3.0 引進 ScopedDeployment</span><span class="sxs-lookup"><span data-stu-id="6543a-1288">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1289">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1289">Az.Sql</span></span>
* <span data-ttu-id="6543a-1290">已將 PublicNetworkAccess 新增至 'New-AzSqlServer' 和 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1290">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="6543a-1291">已針對受控資料庫新增對於長期保留備份設定的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1291">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="6543a-1292">在受控資料庫上取得/設定 LTR 原則</span><span class="sxs-lookup"><span data-stu-id="6543a-1292">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="6543a-1293">依受控資料庫、受控執行個體或位置取得 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="6543a-1293">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="6543a-1294">移除 LTR 備份</span><span class="sxs-lookup"><span data-stu-id="6543a-1294">Remove an LTR backup</span></span>
    - <span data-ttu-id="6543a-1295">還原 LTR 備份以建立新的受控資料庫</span><span class="sxs-lookup"><span data-stu-id="6543a-1295">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="6543a-1296">已將 MinimalTlsVersion 新增至 New-AzSqlServer 和 Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="6543a-1296">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="6543a-1297">已將 MinimalTlsVersion 新增至 New-AzSqlInstance 和 Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-1297">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="6543a-1298">已提高適用於 Az.Network 的 SQL SDK 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-1298">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1299">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1299">Az.Storage</span></span>
* <span data-ttu-id="6543a-1300">已在 ImmutabilityPolicy 中支援 AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="6543a-1300">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="6543a-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-1301">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="6543a-1302">已針對未來版本中的 AzureStorageTable 類型變更新增重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-1302">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="6543a-1303">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-1303">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="6543a-1304">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="6543a-1304">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1305">Az.Websites</span></span>
* <span data-ttu-id="6543a-1306">已為 'New-AzAppServicePlan' 和 'Set-AzAppServicePlan' 新增標籤參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1306">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="6543a-1307">將自訂網域新增至網站時如果擲回例外狀況，則會停止執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1307">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="6543a-1308">已新增支援而可針對未和 App Service 方案位於相同資源群組中的 App Service 執行作業</span><span class="sxs-lookup"><span data-stu-id="6543a-1308">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="6543a-1309">已將存取限制套用至不同資源群組中的 WebApp/函式</span><span class="sxs-lookup"><span data-stu-id="6543a-1309">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="6543a-1310">已修正為 WebAppSlots 設定自訂主機名稱的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1310">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="6543a-1311">3.5.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1311">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-1312">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-1313">更新用戶端遙測。</span><span class="sxs-lookup"><span data-stu-id="6543a-1313">Updated client side telemetry.</span></span>
* <span data-ttu-id="6543a-1314">Az.IotHub 已新增 Cmdlet 來支援裝置管理。</span><span class="sxs-lookup"><span data-stu-id="6543a-1314">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="6543a-1315">Az.SqlVirtualMachine 已新增用於可用性群組接聽程式的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1315">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1316">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1316">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1317">已將 SubscriptionId、TenantId 和執行時間新增至用戶端遙測的資料</span><span class="sxs-lookup"><span data-stu-id="6543a-1317">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-1318">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-1318">Az.Automation</span></span>
* <span data-ttu-id="6543a-1319">已修正 'New-AzAutomationSoftwareUpdateConfiguration' 參考文件中範例 1 的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-1319">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-1320">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1320">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-1321">已將 SDK 更新至 7.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1321">Updated SDK to 7.0</span></span>
* <span data-ttu-id="6543a-1322">已改善伺服器回應空白主體時的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-1322">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1323">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1323">Az.Compute</span></span>
* <span data-ttu-id="6543a-1324">已允許 ProximityPlacementGroupId 在更新期間為空白值</span><span class="sxs-lookup"><span data-stu-id="6543a-1324">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-1325">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-1325">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-1326">已新增 Cmdlet 來取得可在 WAF 中使用的受控規則定義</span><span class="sxs-lookup"><span data-stu-id="6543a-1326">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1327">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1327">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1328">已新增在 IoT 中樞中管理裝置的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1328">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="6543a-1329">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1329">New Cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1330">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1330">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1331">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1331">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1332">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1332">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="6543a-1333">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="6543a-1333">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-1334">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1334">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-1335">已修正 Add-AzKeyVaultKey.md 的重複文字</span><span class="sxs-lookup"><span data-stu-id="6543a-1335">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1336">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1336">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1337">已修正 Get-AzLog Cmdlet 的描述。</span><span class="sxs-lookup"><span data-stu-id="6543a-1337">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="6543a-1338">已將名為 ActionGroupI 的新參數新增至 'New-AzMetricAlertRuleV2' 命令。</span><span class="sxs-lookup"><span data-stu-id="6543a-1338">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="6543a-1339">使用者可以提供 ActionGroupId(string) 或 ActionGorup(ActivityLogAlertActionGroup)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1339">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1340">Az.Network</span></span>
* <span data-ttu-id="6543a-1341">已為 'New-AzPrivateLinkService' Cmdlet 的參數 '-EnableProxyProtocol' 新增一個額外的參數附註。</span><span class="sxs-lookup"><span data-stu-id="6543a-1341">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="6543a-1342">已修正 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中的 FilterData 範例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1342">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6543a-1343">已新增封包擷取範例，可在 Start-AzVirtualNetworkGatewayConnectionPacketCapture.md 和 Start-AzVirtualnetworkGatewayPacketCapture.md 中擷取所有內部和外部封包。</span><span class="sxs-lookup"><span data-stu-id="6543a-1343">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="6543a-1344">支援 VNet 防火牆上的 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="6543a-1344">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="6543a-1345">未新增任何 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1345">No new cmdlets are added.</span></span> <span data-ttu-id="6543a-1346">放寬 VNet 防火牆上的防火牆原則限制</span><span class="sxs-lookup"><span data-stu-id="6543a-1346">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1347">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1347">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1348">已為 SQL Database 新增「還原為檔案」支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1348">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1349">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1349">Az.Resources</span></span>
* <span data-ttu-id="6543a-1350">已重構範本部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1350">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="6543a-1351">已新增用於在管理群組上管理部署的 Cmdlet：\*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6543a-1351">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="6543a-1352">已新增用於在租用戶範圍上管理部署的 Cmdlet：\*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="6543a-1352">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="6543a-1353">已重構 \*-AzDeployment Cmdlet，以便在特定訂用帳戶範圍內工作</span><span class="sxs-lookup"><span data-stu-id="6543a-1353">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="6543a-1354">為 \*-AzDeployment Cmdlet 建立別名 \*-AzSubscriptionDeployment</span><span class="sxs-lookup"><span data-stu-id="6543a-1354">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="6543a-1355">已修正未設定參數 'AvailableToOtherTenants' 時的 'Update-AzADApplication'</span><span class="sxs-lookup"><span data-stu-id="6543a-1355">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="6543a-1356">已移除 ApplicationObjectWithoutCredentialParameterSet 來避免 AmbiguousParameterSetException。</span><span class="sxs-lookup"><span data-stu-id="6543a-1356">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="6543a-1357">已重新產生說明檔</span><span class="sxs-lookup"><span data-stu-id="6543a-1357">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1358">Az.Sql</span></span>
* <span data-ttu-id="6543a-1359">已在受控執行個體上新增跨訂用帳戶的時間點還原支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1359">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="6543a-1360">已新增變更現有 SQL 受控執行個體硬體世代的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1360">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="6543a-1361">已修正 'Update-AzSqlServerVulnerabilityAssessmentSetting' 說明範例：parameter/property output - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="6543a-1361">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6543a-1362">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6543a-1362">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6543a-1363">已新增用於可用性群組接聽程式的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1363">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6543a-1364">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6543a-1364">Az.StorageSync</span></span>
* <span data-ttu-id="6543a-1365">已更新 'Invoke-AzStorageSyncCompatibilityCheck' 中支援的字元集。</span><span class="sxs-lookup"><span data-stu-id="6543a-1365">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="6543a-1366">3.4.0 - 2020 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1366">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-1367">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-1367">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-1368">Az.CosmosDB 初始版本 0.1.0 已發行</span><span class="sxs-lookup"><span data-stu-id="6543a-1368">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="6543a-1369">Az.Network ConnectionMonitor V2 支援已新增</span><span class="sxs-lookup"><span data-stu-id="6543a-1369">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1370">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1370">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1371">當 AzureRmContext.json 無法使用時，停用內容自動儲存</span><span class="sxs-lookup"><span data-stu-id="6543a-1371">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="6543a-1372">將 Azure Powershell Common 的參考更新至 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="6543a-1372">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-1373">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-1373">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-1374">**Get-AzApiManagementApiSchema** 已修正取得與 API 相關聯的 Open-Api 結構描述   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="6543a-1374">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="6543a-1375">**New-AzApiManagementProduct** _ 和 _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="6543a-1375">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="6543a-1376"> https://github.com/Azure/azure-powershell/issues/10472 的修正文件</span><span class="sxs-lookup"><span data-stu-id="6543a-1376">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="6543a-1377">**Set-AzApiManagementApi** 新增的範例，示範如何使用 Cmdlet 來更新 ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6543a-1377">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1378">Az.Compute</span></span>
* <span data-ttu-id="6543a-1379">將 VM 狀態的數目限制為 100，以避免在沒有 VM 名稱的情況下執行 Get-AzVM -Status 時進行節流。</span><span class="sxs-lookup"><span data-stu-id="6543a-1379">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="6543a-1380">新增 Update-AzDiskEncryptionSet Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1380">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="6543a-1381">將 EncryptionType 和 DiskEncryptionSetId 參數新增至下列 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1381">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="6543a-1382">New-AzDiskUpdateConfig、New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1382">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="6543a-1383">將 ColocationStatus 參數新增至 Get-AzProximityPlacementGroup Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1383">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1384">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1384">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1385">將 ADF .Net SDK 版本更新為 4.7.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1385">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6543a-1386">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6543a-1386">Az.DeploymentManager</span></span>
* <span data-ttu-id="6543a-1387">新增資源的 LIST 作業</span><span class="sxs-lookup"><span data-stu-id="6543a-1387">Adds LIST operations for resources</span></span>
* <span data-ttu-id="6543a-1388">新增執行健康情況檢查步驟作業的功能</span><span class="sxs-lookup"><span data-stu-id="6543a-1388">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-1389">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-1389">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-1390">修正 New-AzHDInsightCluster 的文件錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-1390">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-1391">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1391">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-1392">將 Name 別名新增至 VaultName 屬性，使 Remove-AzureKeyVault 與 New-AzureKeyVault 一致。</span><span class="sxs-lookup"><span data-stu-id="6543a-1392">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1393">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1393">Az.Network</span></span>
* <span data-ttu-id="6543a-1394">新增至 Set-AzNetworkWatcherConfigFlowLog.md 以示範流量分析停用案例的新範例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1394">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="6543a-1395">新增將管理 IP 設定指派給 Azure 防火牆的支援 - 防火牆將用於其管理流量的專用子網路和公用 IP</span><span class="sxs-lookup"><span data-stu-id="6543a-1395">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="6543a-1396">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1396">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6543a-1397">已新增可接受公用 IP 位址物件的參數 -ManagementPublicIpAddress (非強制)</span><span class="sxs-lookup"><span data-stu-id="6543a-1397">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="6543a-1398">已在防火牆物件上新增方法 SetManagementIpConfiguration - 需要子網路和公用 IP 位址作為輸入 - 子網路名稱必須是 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="6543a-1398">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="6543a-1399">已更正 Get-AzNetworkSecurityGroup 範例，以顯示 NSG (不是網路介面) 的範例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1399">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="6543a-1400">已修正 New-AzVpnSite 命令中，導致資源識別碼完成器無法完成參數的錯字。</span><span class="sxs-lookup"><span data-stu-id="6543a-1400">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="6543a-1401">已在應用程式閘道中新增重寫規則動作集內 URL 設定的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1401">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="6543a-1402">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1402">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-1403">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="6543a-1404">使用選擇性參數 UrlConfiguration 更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1404">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="6543a-1405">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6543a-1405">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="6543a-1406">新增對於 NetworkWatcher ConnectionMonitor 第 2 版資源的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1406">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-1407">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-1407">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-1408">支援在決定要補救的資源之前，評估合規性</span><span class="sxs-lookup"><span data-stu-id="6543a-1408">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="6543a-1409">將 '-ResourceDiscoverMode' 參數新增至 Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="6543a-1409">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="6543a-1410">新增 Get-AzPolicyMetadata Cmdlet 以取得原則中繼資料資源</span><span class="sxs-lookup"><span data-stu-id="6543a-1410">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="6543a-1411">已更新 API 版本 2019-10-01 的 Get-AzPolicyState 和 Get-AzPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="6543a-1411">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1412">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1412">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1413">Azure Site Recovery 支援移除已複寫的磁碟。</span><span class="sxs-lookup"><span data-stu-id="6543a-1413">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="6543a-1414">Azure 備份在建立復原服務保存庫時新增了新增標記的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1414">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1415">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1415">Az.Resources</span></span>
* <span data-ttu-id="6543a-1416">以內容訂閱的預設值，讓 \*-AzPolicyAssignment Cmdlet 中的 -Scope 成為選擇性</span><span class="sxs-lookup"><span data-stu-id="6543a-1416">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="6543a-1417">新增使用密碼和金鑰認證建立 ADServicePrincipal 的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1417">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1418">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1418">Az.Sql</span></span>
<span data-ttu-id="6543a-1419">修正 New-AzSqlDatabaseSecondary Cmdlet 來檢查 PartnerDatabaseName 是否存在，而不是 DatabaseName 是否存在。</span><span class="sxs-lookup"><span data-stu-id="6543a-1419">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1420">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1420">Az.Storage</span></span>
* <span data-ttu-id="6543a-1421">支援在建立儲存體帳戶中設定資料表/佇列加密 Keytype</span><span class="sxs-lookup"><span data-stu-id="6543a-1421">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="6543a-1422">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-1422">New-AzStorageAccount</span></span>
* <span data-ttu-id="6543a-1423">在 StorageException 沒有 ExtendedErrorInformation 時顯示 RequestId</span><span class="sxs-lookup"><span data-stu-id="6543a-1423">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="6543a-1424">修正 Cmdlet Start-AzStorageBlobCopy 的範例 6</span><span class="sxs-lookup"><span data-stu-id="6543a-1424">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1425">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1425">Az.Websites</span></span>
* <span data-ttu-id="6543a-1426">Set-AzWebapp 和 Set-AzWebappSlot 支援 AlwaysOn、MinTls 和 FtpsState 屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1426">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="6543a-1427">修正在使用單一 Set-AzWebApp 命令的同時設定 HttpsOnly 和變更 AppservicePlan，將 HttpsOnly 重設為預設值的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1427">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="6543a-1428">3.3.0 - 2020 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1428">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-1429">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1429">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1430">已更新 Add-AzEnvironment 和 Set-AzEnvironment 以接受 AzureAttestationServiceEndpointResourceId 和 AzureAttestationServiceEndpointSuffix 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1430">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-1431">Az.Cdn</span></span>
* <span data-ttu-id="6543a-1432">在 New-AzCdnEndpoint Cmdlet 中顯示錯誤回應詳細資料</span><span class="sxs-lookup"><span data-stu-id="6543a-1432">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1433">Az.Compute</span></span>
* <span data-ttu-id="6543a-1434">修正具有受控 OD 磁碟 (沒有 OS 設定檔) 之 VM 的 Set-AzVMCustomScriptExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1434">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6543a-1435">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-1435">Az.ContainerInstance</span></span>
* <span data-ttu-id="6543a-1436">修正了 New-AzContainerGroup 範例所使用的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-1436">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6543a-1437">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6543a-1437">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6543a-1438">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1438">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6543a-1439">取得 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6543a-1439">Get the Edge Storage Container</span></span>
* <span data-ttu-id="6543a-1440">新增了 Cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1440">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6543a-1441">建立新的 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6543a-1441">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="6543a-1442">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1442">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6543a-1443">移除 Edge 儲存體容器</span><span class="sxs-lookup"><span data-stu-id="6543a-1443">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="6543a-1444">新增了 Cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="6543a-1444">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="6543a-1445">用來重新整理 Edge 儲存體容器資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="6543a-1445">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="6543a-1446">新增了 Cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1446">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6543a-1447">取得 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1447">Get the Edge Storage Account</span></span>
* <span data-ttu-id="6543a-1448">新增了 Cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1448">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6543a-1449">建立新的 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1449">Create new Edge Storage Account</span></span>
* <span data-ttu-id="6543a-1450">新增了 Cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="6543a-1450">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="6543a-1451">移除 Edge 儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1451">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="6543a-1452">叫用 Cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="6543a-1452">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="6543a-1453">用來重新整理共用資料的叫用動作</span><span class="sxs-lookup"><span data-stu-id="6543a-1453">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="6543a-1454">新增了 Cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="6543a-1454">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="6543a-1455">設定 az databoxedge 儲存體帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="6543a-1455">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1456">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1457">新增適用於 Get-AzDataFactoryV2IntegrationRuntime Cmd 的 AutoUpdateETA、LatestVersion、PushedVersion、TaskQueueId 和 VersionStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-1457">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="6543a-1458">將 ADF .Net SDK 版本更新為 4.6.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1458">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="6543a-1459">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'PublicIPs'，以使用靜態公用 IP 位址建立 Azure-SSIS IR。</span><span class="sxs-lookup"><span data-stu-id="6543a-1459">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="6543a-1460">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="6543a-1460">Az.DevTestLabs</span></span>
* <span data-ttu-id="6543a-1461">移除 Get-AzDtlAllowedVMSizesPolicy.md 中中斷的連結</span><span class="sxs-lookup"><span data-stu-id="6543a-1461">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-1462">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1462">Az.EventHub</span></span>
* <span data-ttu-id="6543a-1463">問題 10634 的修正內容：修正 Null 物件參考以移除 eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="6543a-1463">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-1464">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-1464">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-1465">修正 Invoke-AzHDInsightHiveJob.md 錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-1465">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6543a-1466">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6543a-1466">Az.MachineLearning</span></span>
* <span data-ttu-id="6543a-1467">由於不再提供 MachineLearningCompute，已移除下列 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1467">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="6543a-1468">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6543a-1468">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="6543a-1469">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="6543a-1469">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="6543a-1470">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6543a-1470">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="6543a-1471">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6543a-1471">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="6543a-1472">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="6543a-1472">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="6543a-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="6543a-1473">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="6543a-1474">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="6543a-1474">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1475">Az.Network</span></span>
* <span data-ttu-id="6543a-1476">將 Microsoft.Azure.Management.Sql 相依性從 1.36-preview 升級到 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="6543a-1476">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1477">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1477">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1478">Azure Site Recovery 對使用 Azure 至 Azure 提供者的客戶受控金鑰進行待用加密的受控磁碟 VM 支援變更。</span><span class="sxs-lookup"><span data-stu-id="6543a-1478">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="6543a-1479">Azure Site Recovery 支援將磁碟加密集識別碼輸入為選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="6543a-1479">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6543a-1480">Azure Site Recovery 支援將磁碟加密集識別碼輸入為磁碟層級的選擇性輸入，以啟用 VMware 至 Azure 的保護。</span><span class="sxs-lookup"><span data-stu-id="6543a-1480">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="6543a-1481">Azure Site Recovery 支援以將適用於 HyperV 的磁碟加密集對應更新至 Azure 的複寫受保護項目。</span><span class="sxs-lookup"><span data-stu-id="6543a-1481">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1482">Az.Resources</span></span>
* <span data-ttu-id="6543a-1483">修正 'Remove-AzTag' 說明文件中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-1483">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1484">Az.Sql</span></span>
* <span data-ttu-id="6543a-1485">修正弱點評定設定基準 Cmdlet 功能，以在 Azure 資料庫的主要資料庫中運作，並在受控執行個體系統資料庫中加以限制。</span><span class="sxs-lookup"><span data-stu-id="6543a-1485">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="6543a-1486">修正建立 SQL 執行個體容錯移轉群組時的錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-1486">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="6543a-1487">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6543a-1487">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="6543a-1488">將 DR 新增為新的有效授權類型</span><span class="sxs-lookup"><span data-stu-id="6543a-1488">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1489">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1489">Az.Storage</span></span>
* <span data-ttu-id="6543a-1490">在後續版本中新增 DefaultAction 值變更的重大變更警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-1490">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="6543a-1491">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-1491">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="6543a-1492">使用參數 -IncludeGeoReplicationStats 執行 get-AzureRMStorageAccount，支援取得儲存體帳戶的上次同步處理時間</span><span class="sxs-lookup"><span data-stu-id="6543a-1492">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="6543a-1493">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-1493">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="6543a-1494">3.2.0 - 2019 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1494">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="6543a-1495">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-1495">General</span></span>
* <span data-ttu-id="6543a-1496">更新 .psd1 中的更新參考，以便所有模組均可使用相對路徑</span><span class="sxs-lookup"><span data-stu-id="6543a-1496">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1497">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1497">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1498">針對 Az 4.0 預覽的用戶端遙測設定正確的 UserAgent</span><span class="sxs-lookup"><span data-stu-id="6543a-1498">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="6543a-1499">當 Az 4.0 預覽中的內容為 null 時，顯示使用者易記的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-1499">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-1500">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-1500">Az.Batch</span></span>
* <span data-ttu-id="6543a-1501">修正問題 [#10602](https://github.com/Azure/azure-powershell/issues/10602)，其中 **New-AzBatchPool** 並未適當地將 'VirtualMachineConfiguration.ContainerConfiguration' 或 'VirtualMachineConfiguration.DataDisks' 傳送到伺服器。</span><span class="sxs-lookup"><span data-stu-id="6543a-1501">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1502">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1502">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1503">將 ADF .Net SDK 版本更新為 4.5.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1503">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-1504">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-1504">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-1505">已新增 WAF 受控規則排除支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1505">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="6543a-1506">在自動完成中新增 SocketAddr</span><span class="sxs-lookup"><span data-stu-id="6543a-1506">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6543a-1507">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6543a-1507">Az.HealthcareApis</span></span>
* <span data-ttu-id="6543a-1508">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="6543a-1508">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-1509">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-1509">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-1510">已修正存取可能未設定的值時發生的錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-1510">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="6543a-1511">橢圓曲線密碼編譯憑證管理</span><span class="sxs-lookup"><span data-stu-id="6543a-1511">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="6543a-1512">已新增為憑證原則指定 Curve 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1512">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1513">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1514">在 Add Diagnostic Settings 命令中新增選用的引數。</span><span class="sxs-lookup"><span data-stu-id="6543a-1514">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="6543a-1515">如果存在切換引數，表示匯出到 Log Analytics 必須是固定的結構描述 (也稱為</span><span class="sxs-lookup"><span data-stu-id="6543a-1515">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="6543a-1516">專用，資料類型)</span><span class="sxs-lookup"><span data-stu-id="6543a-1516">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1517">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1517">Az.Network</span></span>
* <span data-ttu-id="6543a-1518">在 AzureFirewall 應用程式、Nat 和網路規則中支援 IpGroups。</span><span class="sxs-lookup"><span data-stu-id="6543a-1518">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1519">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1519">Az.Resources</span></span>
* <span data-ttu-id="6543a-1520">修正如果範本名稱與一些內建參數名稱衝突，則範本部署無法讀取範本參數的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1520">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="6543a-1521">更新原則 Cmdliet 以使用新的 API 版本 2019-09-01，其中引進原則集合定義內的群組支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1521">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1522">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1522">Az.Sql</span></span>
* <span data-ttu-id="6543a-1523">已將弱點評估自動啟用中的儲存體建立升級為 StorageV2</span><span class="sxs-lookup"><span data-stu-id="6543a-1523">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1524">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1524">Az.Storage</span></span>
* <span data-ttu-id="6543a-1525">支援使用以 Oauth 驗證為基礎的儲存體內容來產生 Blob/Constainer Idenity 為基礎的 SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-1525">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="6543a-1526">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="6543a-1526">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="6543a-1527">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6543a-1527">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="6543a-1528">支援撤銷儲存體帳戶使用者委派金鑰，因此會撤銷所有 Idenity SAS 權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-1528">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="6543a-1529">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="6543a-1529">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="6543a-1530">升級至 Microsoft.Azure.Management.Storage 14.2.0，以支援新的 API 版本 2019-06-01。</span><span class="sxs-lookup"><span data-stu-id="6543a-1530">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="6543a-1531">針對檔案共用 Cmdlet 的管理平面中超過 5120 的值支援 QuotaGiB (Gibibye 中的共用配額)，並將 'Quota' 參數別名新增到 'QuotaGiB' 參數中。</span><span class="sxs-lookup"><span data-stu-id="6543a-1531">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="6543a-1532">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1532">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="6543a-1533">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1533">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="6543a-1534">在參數 'Quota' 中新增參數別名 'QuotaGiB'</span><span class="sxs-lookup"><span data-stu-id="6543a-1534">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="6543a-1535">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="6543a-1535">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="6543a-1536">修正 Set-AzStorageContainerAcl 可清除已儲存之存取原則的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1536">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="6543a-1537">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="6543a-1537">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="6543a-1538">3.1.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1538">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-1539">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-1539">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-1540">已發佈 Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1540">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="6543a-1541">已發佈 Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1541">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1542">Az.Compute</span></span>
* <span data-ttu-id="6543a-1543">VM Reapply 功能</span><span class="sxs-lookup"><span data-stu-id="6543a-1543">VM Reapply feature</span></span>
    - <span data-ttu-id="6543a-1544">將 Reapply 參數新增到 Set-AzVM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1544">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="6543a-1545">VM 擴展集 AutomaticRepairs 功能：</span><span class="sxs-lookup"><span data-stu-id="6543a-1545">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="6543a-1546">將 EnableAutomaticRepair、AutomaticRepairGracePeriod 和 AutomaticRepairMaxInstanceRepairsPercent 參數新增到下列 Cmdlet： New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6543a-1546">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="6543a-1547">適用於 New-AzVM 的跨租用戶資源庫映像支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1547">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="6543a-1548">將 'Spot' 新增到 New-AzVM、New-AzVMConfig 和 New-AzVmss Cmdlet 中的 Priority 參數引數完成程式</span><span class="sxs-lookup"><span data-stu-id="6543a-1548">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6543a-1549">將 DiskIOPSReadWrite 和 DiskMBpsReadWrite 參數新增到 Add-AzVmssDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1549">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="6543a-1550">將 New-AzGalleryImageVersion Cmdlet 的 SourceImageId 參數變更為選擇性</span><span class="sxs-lookup"><span data-stu-id="6543a-1550">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="6543a-1551">將 OSDiskImage 和 DataDiskImage 參數新增到 New-AzGalleryImageVersion Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1551">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="6543a-1552">將 HyperVGeneration 參數新增到 New-AzGalleryImageDefinition Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1552">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="6543a-1553">將 SkipExtensionsOnOverprovisionedVMs 參數新增到 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1553">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="6543a-1554">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="6543a-1554">Az.DataBoxEdge</span></span>
* <span data-ttu-id="6543a-1555">已新增 Cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6543a-1555">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6543a-1556">取得訂單</span><span class="sxs-lookup"><span data-stu-id="6543a-1556">Get the Order</span></span>
* <span data-ttu-id="6543a-1557">已新增 Cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6543a-1557">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6543a-1558">建立新訂單</span><span class="sxs-lookup"><span data-stu-id="6543a-1558">Create new Order</span></span>
* <span data-ttu-id="6543a-1559">已新增 Cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="6543a-1559">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="6543a-1560">移除訂單</span><span class="sxs-lookup"><span data-stu-id="6543a-1560">Remove the Order</span></span>
* <span data-ttu-id="6543a-1561">Cmdlet `New-AzDataBoxEdgeShare` 中的變更</span><span class="sxs-lookup"><span data-stu-id="6543a-1561">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="6543a-1562">立即建立本機共用</span><span class="sxs-lookup"><span data-stu-id="6543a-1562">Now creates Local Share</span></span>
* <span data-ttu-id="6543a-1563">已新增 Cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="6543a-1563">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="6543a-1564">IotRole 現在對應到共用</span><span class="sxs-lookup"><span data-stu-id="6543a-1564">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="6543a-1565">已新增 Cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="6543a-1565">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="6543a-1566">在裝置上叫用掃描更新、下載更新並安裝更新</span><span class="sxs-lookup"><span data-stu-id="6543a-1566">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="6543a-1567">已新增 Cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6543a-1567">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6543a-1568">取得觸發程序的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-1568">Gets the information about Triggers</span></span>
* <span data-ttu-id="6543a-1569">已新增 Cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6543a-1569">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6543a-1570">建立新的觸發程序</span><span class="sxs-lookup"><span data-stu-id="6543a-1570">Create new Triggers</span></span>
* <span data-ttu-id="6543a-1571">已新增 Cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="6543a-1571">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="6543a-1572">移除觸發程序</span><span class="sxs-lookup"><span data-stu-id="6543a-1572">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1573">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1573">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1574">將 ADF .Net SDK 版本更新為 4.4.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1574">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="6543a-1575">為 'Set-AzureRmDataFactoryV2IntegrationRuntime' CMD 新增參數 'ExpressCustomSetup'，以在無需自訂設定指令碼的情況下啟用設定組態和第三方元件。</span><span class="sxs-lookup"><span data-stu-id="6543a-1575">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-1576">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-1576">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-1577">更新 Get-AzDataLakeStoreDeletedItem 和 Restore-AzDataLakeStoreDeletedItem 的文件</span><span class="sxs-lookup"><span data-stu-id="6543a-1577">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-1578">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1578">Az.EventHub</span></span>
* <span data-ttu-id="6543a-1579">修正 10301 的問題：修正 SAS 權杖日期格式</span><span class="sxs-lookup"><span data-stu-id="6543a-1579">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-1580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-1580">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-1581">將 MinimumTlsVersion 參數新增到 Enable-AzFrontDoorCustomDomainHttps 和 New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="6543a-1581">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="6543a-1582">將 HealthProbeMethod 和 EnabledState 參數新增到 New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="6543a-1582">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="6543a-1583">新增新的 cmdlet 以建立 BackendPoolsSettings 物件，以傳遞到 Front Door 的建立/更新</span><span class="sxs-lookup"><span data-stu-id="6543a-1583">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="6543a-1584">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="6543a-1584">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1585">Az.Network</span></span>
* <span data-ttu-id="6543a-1586">變更 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' 和 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData 選項範例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1586">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="6543a-1587">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="6543a-1587">Az.PrivateDns</span></span>
* <span data-ttu-id="6543a-1588">已將 PrivateDns .net SDK 更新為 1.0.0 版</span><span class="sxs-lookup"><span data-stu-id="6543a-1588">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1589">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1589">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1590">Azure Site Recovery 支援在啟用保護時選取磁碟類型。</span><span class="sxs-lookup"><span data-stu-id="6543a-1590">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="6543a-1591">Azure Site Recovery 復原計劃針對動作編輯的錯誤 (bug) 修正。</span><span class="sxs-lookup"><span data-stu-id="6543a-1591">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="6543a-1592">Azure 備份 SQL 還原支援接受 filestream DB.</span><span class="sxs-lookup"><span data-stu-id="6543a-1592">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6543a-1593">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6543a-1593">Az.RedisCache</span></span>
* <span data-ttu-id="6543a-1594">已在 'New-AzRedisCache' 和 'Set-AzRedisCache' Cmdlet 中新增了 'MinimumTlsVersion'參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-1594">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="6543a-1595">此外，也在 'Get-AzRedisCache' Cmdlet 的輸出中新增了 'MinimumTlsVersion'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1595">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="6543a-1596">已針對 'Set-AzRedisCache' 和 'New-AzRedisCache' Cmdlet 新增了 '-Size' 參數的驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-1596">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1597">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1597">Az.Resources</span></span>
- <span data-ttu-id="6543a-1598">更新了原則 Cmdlet 以使用新的 API 版本 2019-06-01，其在原則指派中具有新的 EnforcementMode 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1598">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="6543a-1599">更新了建立原則定義說明範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1599">Updated create policy definition help example</span></span>
- <span data-ttu-id="6543a-1600">修正錯誤 (bug) Remove-AZADServicePrincipal -ServicePrincipalName，當找不到服務主體名稱時擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="6543a-1600">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="6543a-1601">修正錯誤 (bug) New-AZADServicePrincipal，當租用戶沒有任何訂用帳戶擲回 Null 參考。</span><span class="sxs-lookup"><span data-stu-id="6543a-1601">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="6543a-1602">將 New-azadserviceprincipal 變更為只將認證新增到相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6543a-1602">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1603">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1603">Az.Sql</span></span>
* <span data-ttu-id="6543a-1604">新增了對 ReadReplicaCount 資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1604">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="6543a-1605">修正了未設定區域備援時的 Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6543a-1605">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="6543a-1606">3.0.0 - 2019 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1606">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="6543a-1607">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-1607">General</span></span>
* <span data-ttu-id="6543a-1608">已發行 Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1608">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1609">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1609">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1610">為 'Resolve-Error' 別名新增了淘汰訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-1610">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6543a-1611">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6543a-1611">Az.Advisor</span></span>
* <span data-ttu-id="6543a-1612">已為 Get-AzAdvisorRecommendation Cmdlet 新增了新的 'Operational Excellence' 類別。</span><span class="sxs-lookup"><span data-stu-id="6543a-1612">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-1613">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-1613">Az.Batch</span></span>
* <span data-ttu-id="6543a-1614">已將 `BatchAccountContext` 中的 `CoreQuota` 重新命名為 `DedicatedCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1614">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="6543a-1615">另外還有新的 `LowPriorityCoreQuota`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1615">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="6543a-1616">這會影響 **Get-AzBatchAccount** 。</span><span class="sxs-lookup"><span data-stu-id="6543a-1616">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="6543a-1617">**New-AzBatchTask** `-ResourceFile` 參數現在會採用 `PSResourceFile` 物件集合，可使用新的 **New-AzBatchResourceFile** Cmdlet 加以建構。</span><span class="sxs-lookup"><span data-stu-id="6543a-1617">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="6543a-1618">新增 **New-AzBatchResourceFile** Cmdlet 以協助建立 `PSResourceFile` 物件。</span><span class="sxs-lookup"><span data-stu-id="6543a-1618">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="6543a-1619">這些可以提供給 `-ResourceFile` 參數中的 **New-AzBatchTask** 。</span><span class="sxs-lookup"><span data-stu-id="6543a-1619">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="6543a-1620">除了現有的 `HttpUrl` 方式，這也會支援兩種新的資源檔類型：</span><span class="sxs-lookup"><span data-stu-id="6543a-1620">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="6543a-1621">`AutoStorageContainerName` 以資源檔為基礎，會將整個自動儲存體容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="6543a-1621">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="6543a-1622">`StorageContainerUrl` 以資源檔為基礎，會將 URL 中指定的容器下載至 Batch-節點。</span><span class="sxs-lookup"><span data-stu-id="6543a-1622">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="6543a-1623">已移除 **AzBatchApplication** 所傳回之 `PSApplication` 的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1623">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6543a-1624">您現在可以使用 **AzBatchApplicationPackage** 來取出應用程式內的特定套件。</span><span class="sxs-lookup"><span data-stu-id="6543a-1624">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="6543a-1625">例如： `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication` 。</span><span class="sxs-lookup"><span data-stu-id="6543a-1625">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="6543a-1626">將 **Get-AzBatchApplicationPackage** 、 **New-AzBatchApplicationPackage** 、 **Remove-AzBatchApplicationPackage** 、 **Get-AzBatchApplication** 、 **New-AzBatchApplication** 、 **Remove-AzBatchApplication** 和 **Set-AzBatchApplication** 上的 `ApplicationId` 重新命名為 `ApplicationName`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1626">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="6543a-1627">`ApplicationId` 現在是 `ApplicationName` 的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1627">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="6543a-1628">已在 `PSWindowsUserConfiguration` 中新增新的 `PSUserAccount` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1628">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="6543a-1629">已將 `PSApplicationPackage` 上的 `Version` 重新命名為 `Name`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1629">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="6543a-1630">已將 `PSResourceFile` 上的 `BlobSource` 重新命名為 `HttpUrl`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1630">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="6543a-1631">已從 `PSVirtualMachineConfiguration` 移除 `OSDisk` 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-1631">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="6543a-1632">已移除 **AzBatchPoolOSVersion** 。</span><span class="sxs-lookup"><span data-stu-id="6543a-1632">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="6543a-1633">不再支援此作業。</span><span class="sxs-lookup"><span data-stu-id="6543a-1633">This operation is no longer supported.</span></span>
* <span data-ttu-id="6543a-1634">已從下列 `PSCloudServiceConfiguration` 中移除 `TargetOSVersion`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1634">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6543a-1635">已將 `PSCloudServiceConfiguration` 上的 `CurrentOSVersion` 重新命名為 `OSVersion`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1635">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="6543a-1636">已從 `PSPoolUsageMetrics` 移除 `DataEgressGiB` 和 `DataIngressGiB`。</span><span class="sxs-lookup"><span data-stu-id="6543a-1636">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="6543a-1637">已移除 **AzBatchNodeAgentSku** ，並以 **AzBatchSupportedImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="6543a-1637">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="6543a-1638">**AzBatchSupportedImage** 會傳回與 **AzBatchNodeAgentSku** 相同但格式較好用的資料。</span><span class="sxs-lookup"><span data-stu-id="6543a-1638">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="6543a-1639">系統現在也會傳回新的未驗證映像。</span><span class="sxs-lookup"><span data-stu-id="6543a-1639">New non-verified images are also now returned.</span></span> <span data-ttu-id="6543a-1640">此外，也包含每個映像的 `Capabilities` 和 `BatchSupportEndOfLife` 的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6543a-1640">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="6543a-1641">新增了一項功能，可透過 **New-azbatchpool** 的新 `MountConfiguration` 參數，在集區的每個節點上裝載遠端檔案系統。</span><span class="sxs-lookup"><span data-stu-id="6543a-1641">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="6543a-1642">現在支援網路安全性規則，根據流量的來源連接埠封鎖對集區的網路存取。</span><span class="sxs-lookup"><span data-stu-id="6543a-1642">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="6543a-1643">這會透過 `PSNetworkSecurityGroupRule`上的 `SourcePortRanges` 屬性來完成。</span><span class="sxs-lookup"><span data-stu-id="6543a-1643">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="6543a-1644">執行容器時，Batch 現在支援在容器工作目錄中或 Batch 工作的工作目錄中執行工作。</span><span class="sxs-lookup"><span data-stu-id="6543a-1644">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="6543a-1645">這是由 `PSTaskContainerSettings` 上的 `WorkingDirectory` 屬性所控制。</span><span class="sxs-lookup"><span data-stu-id="6543a-1645">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="6543a-1646">新增了一項功能，可透過新的 `PublicIPs` 屬性，在 `PSNetworkConfiguration` 上指定公用 IP 集合。</span><span class="sxs-lookup"><span data-stu-id="6543a-1646">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="6543a-1647">如此可確保集區中的節點將會有來自清單使用者所提供的 IP。</span><span class="sxs-lookup"><span data-stu-id="6543a-1647">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="6543a-1648">未指定時，`PSSTartTask` 上的 `WaitForSuccess` 預設值現在為 `$True` (之前是 `$False`)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1648">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="6543a-1649">未指定時，`PSAutoUserSpecification` 上的 `Scope` 預設值現在為 `Pool` (之前在 Windows 上是 `Task`，在 Linux 上是 `Pool`)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1649">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-1650">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-1650">Az.Cdn</span></span>
* <span data-ttu-id="6543a-1651">已將 UrlRewriteAction and CacheKeyQueryStringAction 引進 RulesEngine。</span><span class="sxs-lookup"><span data-stu-id="6543a-1651">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="6543a-1652">已修正 AzDeliveryRuleCondition Cmdlet 中的數個錯誤 (bug)，例如遺漏 'Selector’ 輸入。</span><span class="sxs-lookup"><span data-stu-id="6543a-1652">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1653">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1653">Az.Compute</span></span>
* <span data-ttu-id="6543a-1654">磁碟加密集功能</span><span class="sxs-lookup"><span data-stu-id="6543a-1654">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="6543a-1655">新的 Cmdlet： New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6543a-1655">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="6543a-1656">DiskEncryptionSetId 參數已新增至下列 Cmdlet： Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="6543a-1656">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="6543a-1657">DiskEncryptionSetId 和 EncryptionType 參數已新增至下列 Cmdlet： New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1657">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6543a-1658">將 PublicIPAddressVersion 參數新增至 New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1658">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="6543a-1659">將自訂指令碼擴充功能的 FileUris 從公用設定移至受保護的設定</span><span class="sxs-lookup"><span data-stu-id="6543a-1659">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="6543a-1660">將 ScaleInPolicy 新增至 New-AzVmss、New-AzVmssConfig 和 Update-AzVmss Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1660">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="6543a-1661">重大變更</span><span class="sxs-lookup"><span data-stu-id="6543a-1661">Breaking changes</span></span>
    - <span data-ttu-id="6543a-1662">上傳 CreateOption 時，會針對 New-AzDiskConfig 使用 UploadSizeInBytes 參數而非 DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6543a-1662">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="6543a-1663">在 GalleryImageVersion 物件中，會使用 StorageProfile.Source.Id 取代 PublishingProfile.Source.ManagedImage.Id</span><span class="sxs-lookup"><span data-stu-id="6543a-1663">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1664">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1664">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1665">將 ADF .Net SDK 版本更新為 4.3.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1665">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-1666">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-1666">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-1667">更新 ADLS SDK 版本 (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha) ，提供下列修正程式</span><span class="sxs-lookup"><span data-stu-id="6543a-1667">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="6543a-1668">避免在無法將資源回收筒或目錄專案的建立時間還原序列化 (creationtime) 時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6543a-1668">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="6543a-1669">在 adlsclient 中公開每個要求超時設定</span><span class="sxs-lookup"><span data-stu-id="6543a-1669">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="6543a-1670">修正傳遞原始 syncflag 以進行 badoffset 復原</span><span class="sxs-lookup"><span data-stu-id="6543a-1670">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="6543a-1671">修正 EnumerateDirectory 以在檢查回應後取得接續權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-1671">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="6543a-1672">修正 Concat 錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-1672">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-1673">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-1673">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-1674">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1674">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-1675">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-1675">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-1676">修正當使用 Get-AzHDInsightCluster 取得具有 ADLSGen1 儲存體的叢集時，客戶會收到「不是有效的 Base-64 字串」的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1676">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="6543a-1677">將名為 'ApplicationId' 的參數新增至 Add-AzHDInsightClusterIdentity、New-AzHDInsightClusterConfig 和 New-AzHDInsightCluster 三個 Cmdlet 中，讓客戶可以提供服務主體應用程式識別碼來存取 Azure Data Lake。</span><span class="sxs-lookup"><span data-stu-id="6543a-1677">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="6543a-1678">已將 Microsoft.Azure.Management.HDInsight 從 2.1.0 變更為 5.1.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1678">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="6543a-1679">已移除五個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1679">Removed five cmdlets:</span></span>
    - <span data-ttu-id="6543a-1680">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6543a-1680">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6543a-1681">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6543a-1681">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6543a-1682">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="6543a-1682">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="6543a-1683">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6543a-1683">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="6543a-1684">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6543a-1684">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="6543a-1685">新增了三個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1685">Added three cmdlets:</span></span>
    - <span data-ttu-id="6543a-1686">Get-AzHDInsightMonitoring 用來取代 Get-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6543a-1686">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6543a-1687">Enable-AzHDInsightMonitoring 用來取代 Enable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6543a-1687">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="6543a-1688">Disable-AzHDInsightMonitoring 用來取代 Disable-AzHDInsightOMS。</span><span class="sxs-lookup"><span data-stu-id="6543a-1688">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="6543a-1689">修正了 Cmdlet AzHDInsightProperties，以支援來自特定位置的取得功能資訊。</span><span class="sxs-lookup"><span data-stu-id="6543a-1689">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="6543a-1690">已從 Add-AzHDInsightConfigValue 移除參數集 ('Spark1', 'Spark2')。</span><span class="sxs-lookup"><span data-stu-id="6543a-1690">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="6543a-1691">將範例新增至 Cmdlet Add-AzHDInsightSecurityProfile 的說明文件。</span><span class="sxs-lookup"><span data-stu-id="6543a-1691">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="6543a-1692">已變更下列 Cmdlet 的輸出類型：</span><span class="sxs-lookup"><span data-stu-id="6543a-1692">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="6543a-1693">已將 Get-AzHDInsightProperties 的輸出類型從 CapabilitiesResponse 變更為 AzureHDInsightCapabilities。</span><span class="sxs-lookup"><span data-stu-id="6543a-1693">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="6543a-1694">已將 Remove-AzHDInsightCluster 的輸出類型從 ClusterGetResponse 變更為 bool。</span><span class="sxs-lookup"><span data-stu-id="6543a-1694">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="6543a-1695">已將 Set-AzHDInsightGatewaySettings HttpConnectivitySettings 的輸出類型變更為 GatewaySettings。</span><span class="sxs-lookup"><span data-stu-id="6543a-1695">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="6543a-1696">已新增一些狀況測試案例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1696">Added some scenario test cases.</span></span>
* <span data-ttu-id="6543a-1697">移除一些別名：'Add-AzHDInsightConfigValues'、'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="6543a-1697">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1698">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1698">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1699">重大變更：</span><span class="sxs-lookup"><span data-stu-id="6543a-1699">Breaking changes:</span></span>
    - <span data-ttu-id="6543a-1700">Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1700">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6543a-1701">已移除 Cmdlet 'Add-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1701">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6543a-1702">Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1702">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6543a-1703">已移除 Cmdlet 'Get-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1703">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6543a-1704">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1704">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="6543a-1705">已移除類型為 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' 的屬性 'OperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1705">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="6543a-1706">Cmdlet 'New-AzIotHubExportDevice' 已不再支援別名 'New-AzIotHubExportDevices'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1706">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="6543a-1707">Cmdlet 'New-AzIotHubImportDevice' 已不再支援別名 'New-AzIotHubImportDevices'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1707">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="6543a-1708">Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 已不再支援參數 'EventHubEndpointName'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1708">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6543a-1709">已移除 Cmdlet 'Remove-AzIotHubEventHubConsumerGroup' 的參數集 '__AllParameterSets'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1709">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="6543a-1710">Cmdlet 'Set-AzIotHub' 已不再支援參數 'OperationsMonitoringProperties'，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1710">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="6543a-1711">已移除 Cmdlet 'Set-AzIotHub' 的參數集 'UpdateOperationsMonitoringProperties'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1711">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1712">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1712">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1713">Azure Site Recovery 支援將 NSG、公用 IP 和 Azure 的內部負載平衡器網路資源設定為 Azure。</span><span class="sxs-lookup"><span data-stu-id="6543a-1713">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1714">Azure Site Recovery 支援從 VMware 寫入 Azure 受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="6543a-1714">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="6543a-1715">Azure Site Recovery 支援從 VMware 到 Azure 的 NIC 縮減。</span><span class="sxs-lookup"><span data-stu-id="6543a-1715">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="6543a-1716">Azure Site Recovery 支援從 Azure 到 Azure 的加速網路。</span><span class="sxs-lookup"><span data-stu-id="6543a-1716">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1717">Azure Site Recovery 支援從 Azure 到 Azure 的代理程式自動更新。</span><span class="sxs-lookup"><span data-stu-id="6543a-1717">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1718">Azure Site Recovery 支援從 Azure 到 Azure 的標準 SSD。</span><span class="sxs-lookup"><span data-stu-id="6543a-1718">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1719">Azure Site Recovery 支援從 Azure 到 Azure 的 Azure 磁碟加密傳遞。</span><span class="sxs-lookup"><span data-stu-id="6543a-1719">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1720">Azure Site Recovery 提供從 Azure 到 Azure 的新增磁碟保護支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1720">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-1721">已新增 VM 的 SoftDelete 功能，並新增了 SoftDelete 的測試</span><span class="sxs-lookup"><span data-stu-id="6543a-1721">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1722">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1722">Az.Resources</span></span>
* <span data-ttu-id="6543a-1723">將相依性組件 Microsoft.Extensions.Caching.Memory 從1.1.1 更新為 2.2</span><span class="sxs-lookup"><span data-stu-id="6543a-1723">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1724">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1724">Az.Network</span></span>
* <span data-ttu-id="6543a-1725">變更 PrivateEndpointConnection 的所有 Cmdlet，以支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6543a-1725">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="6543a-1726">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1726">Updated cmdlet:</span></span>
        - <span data-ttu-id="6543a-1727">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1727">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-1728">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1728">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-1729">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1729">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-1730">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1730">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-1731">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1731">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6543a-1732">為 PrivateLinkResource 新增新的 Cmdlet，其同時支援一般服務提供者。</span><span class="sxs-lookup"><span data-stu-id="6543a-1732">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="6543a-1733">新的 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1733">New cmdlet:</span></span>
        - <span data-ttu-id="6543a-1734">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="6543a-1734">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="6543a-1735">新增功能 Proxy Protocol V2 的新欄位和參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-1735">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="6543a-1736">在 PrivateLinkService 中新增屬性 EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="6543a-1736">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="6543a-1737">在 PrivateEndpointConnection 中新增屬性 LinkIdentifier</span><span class="sxs-lookup"><span data-stu-id="6543a-1737">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="6543a-1738">更新了 New-AzPrivateLinkService 以新增選擇性參數 EnableProxyProtocol。</span><span class="sxs-lookup"><span data-stu-id="6543a-1738">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="6543a-1739">修正 'New-AzApplicationGatewaySku' 參考文件中不正確的參數描述</span><span class="sxs-lookup"><span data-stu-id="6543a-1739">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="6543a-1740">新增 Cmdlet 以支援 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="6543a-1740">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="6543a-1741">為 VirtualHub的子資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1741">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="6543a-1742">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1742">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1743">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="6543a-1743">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="6543a-1744">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-1744">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6543a-1745">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-1745">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6543a-1746">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-1746">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="6543a-1747">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1747">Set-AzVirtualHub</span></span>
* <span data-ttu-id="6543a-1748">新增 VirtualHub 的新屬性 SKU 和 VirtualWan 的 VirtualWANType 支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1748">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="6543a-1749">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1749">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6543a-1750">New-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="6543a-1750">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6543a-1751">Update-AzVirtualHub：新增了參數 SKU</span><span class="sxs-lookup"><span data-stu-id="6543a-1751">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="6543a-1752">New-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6543a-1752">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="6543a-1753">Update-AzVirtualWan：新增了參數 VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="6543a-1753">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="6543a-1754">為 HubVnetConnection、VpnConnection 和 ExpressRouteConnection 新增 EnableInternetSecurity 屬性的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1754">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="6543a-1755">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1755">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1756">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1756">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="6543a-1757">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1757">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6543a-1758">New-AzureRmVirtualHubVnetConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6543a-1758">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6543a-1759">New-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6543a-1759">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6543a-1760">Update-AzureRmVpnConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6543a-1760">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6543a-1761">New-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6543a-1761">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="6543a-1762">Set-AzureRmExpressRouteConnection：新增了參數 EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="6543a-1762">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="6543a-1763">新增設定 TopLevel WebApplicationFirewall 原則的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1763">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="6543a-1764">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1764">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1765">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="6543a-1765">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="6543a-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="6543a-1766">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="6543a-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="6543a-1767">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="6543a-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="6543a-1768">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="6543a-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="6543a-1769">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="6543a-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-1770">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="6543a-1771">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6543a-1772">New-AzApplicationGatewayFirewallPolicy：新增了參數 PolicySetting、ManagedRule</span><span class="sxs-lookup"><span data-stu-id="6543a-1772">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="6543a-1773">已在 CustomRule 上新增對 Geo-Match 運算子的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1773">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="6543a-1774">已將 GeoMatch 新增至 FirewallCondition 上的運算子</span><span class="sxs-lookup"><span data-stu-id="6543a-1774">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="6543a-1775">已新增 perListener 和 perSite 防火牆原則的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1775">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="6543a-1776">已更新 Cmdlet 中的選用參數 -RewriteRuleSet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1776">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="6543a-1777">New-AzApplicationGatewayHttpListener：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6543a-1777">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="6543a-1778">New-AzApplicationGatewayPathRuleConfig：新增了參數 FirewallPolicy、FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6543a-1778">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="6543a-1779">將 'PSBastion' 中名稱為 AzureBastionSubnet 的必要子網路修正為可不區分大小寫</span><span class="sxs-lookup"><span data-stu-id="6543a-1779">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="6543a-1780">支援網路規則中的目的地 FQDN，以及適用於 Azure 防火牆的 NAT 規則中轉譯的 FQDN</span><span class="sxs-lookup"><span data-stu-id="6543a-1780">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="6543a-1781">為 IpGroup的上層資源 RouteTables 新增支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1781">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="6543a-1782">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1782">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1783">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-1783">New-AzIpGroup</span></span>
        - <span data-ttu-id="6543a-1784">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-1784">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="6543a-1785">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-1785">Get-AzIpGroup</span></span>
        - <span data-ttu-id="6543a-1786">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-1786">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-1787">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-1787">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-1788">移除 Add-AzServiceFabricApplicationCertificate Cmdlet，因為 Add-AzVmssSecret 會涵蓋此案例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1788">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1789">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1789">Az.Sql</span></span>
* <span data-ttu-id="6543a-1790">已新增在受控執行個體上還原已卸載之資料庫的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1790">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="6543a-1791">已從程式碼中淘汰舊版的審核 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1791">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="6543a-1792">移除了已淘汰的別名：</span><span class="sxs-lookup"><span data-stu-id="6543a-1792">Removed deprecated aliases:</span></span>
* <span data-ttu-id="6543a-1793">Get-AzSqlDatabaseIndexRecommendations (改為使用 Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="6543a-1793">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="6543a-1794">Get-AzSqlDatabaseRestorePoints (改為使用 Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="6543a-1794">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="6543a-1795">移除 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1795">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6543a-1796">移除已淘汰的弱點評估設定 Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="6543a-1796">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="6543a-1797">淘汰進階威脅偵測設定 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1797">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="6543a-1798">在 Disable 中新增 Cmdlet 以啟用資料庫中資料行的敏感度建議。</span><span class="sxs-lookup"><span data-stu-id="6543a-1798">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1799">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1799">Az.Storage</span></span>
* <span data-ttu-id="6543a-1800">支援在建立或更新儲存體帳戶時啟用大型檔案共用</span><span class="sxs-lookup"><span data-stu-id="6543a-1800">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="6543a-1801">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-1801">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6543a-1802">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-1802">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6543a-1803">當關閉/取得檔案控制代碼時，跳過檢查輸入路徑是否為檔案目錄或檔案，以避免物件處於 DeletePending 狀態時失敗</span><span class="sxs-lookup"><span data-stu-id="6543a-1803">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="6543a-1804">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6543a-1804">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="6543a-1805">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6543a-1805">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="6543a-1806">2.8.0 - 2019 年10月</span><span class="sxs-lookup"><span data-stu-id="6543a-1806">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="6543a-1807">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-1807">General</span></span>
* <span data-ttu-id="6543a-1808">Az.HealthcareApis 1.0.0 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-1808">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1809">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1809">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1810">針對產生的模組更新遙測和重寫 URL，修正 Windows 單元測試。</span><span class="sxs-lookup"><span data-stu-id="6543a-1810">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-1811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-1811">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-1812">**Set-AzApiManagementApi** - 已新增在 ApiVersionSet 中更新 API 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1812">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="6543a-1813">修正 https://github.com/Azure/azure-powershell/issues/10068 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1813">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-1814">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-1814">Az.Automation</span></span>
* <span data-ttu-id="6543a-1815">已針對 Linux 重新啟動設定參數修正了 New-AzureAutomationSoftwareUpdateConfiguration Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-1815">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-1816">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-1816">Az.Batch</span></span>
* <span data-ttu-id="6543a-1817">**Get-AzBatchNodeAgentSku** 已被取代，在版本 2.0.0 中會由 **Get-AzBatchSupportImage** 取代。</span><span class="sxs-lookup"><span data-stu-id="6543a-1817">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1818">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1818">Az.Compute</span></span>
* <span data-ttu-id="6543a-1819">在 New-AzVM 和 New-AzVmss Cmdlet 中新增 Priority、EvictionPolicy 和 MaxPrice 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1819">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="6543a-1820">修正 Add-AzVMAdditionalUnattendContent 和 Add-AzVMSshPublicKey Cmdlet 的警告訊息和說明文件</span><span class="sxs-lookup"><span data-stu-id="6543a-1820">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="6543a-1821">修正 Linux VM 的 -skipVmBackup 例外狀況，以及 Set-AzVMDiskEncryptionExtension 的受控磁碟。</span><span class="sxs-lookup"><span data-stu-id="6543a-1821">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="6543a-1822">修正 Set-AzVMDiskEncryptionExtension 中更新加密設定中的錯誤 (bug)，兩種傳遞案例。</span><span class="sxs-lookup"><span data-stu-id="6543a-1822">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1823">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1823">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1824">針對 ADF V2 資料流程新增 CRUD 命令：Set-AzDataFactoryV2DataFlow、Remove-AzDataFactoryV2DataFlow 和 Get-AzDataFactoryV2DataFlow。</span><span class="sxs-lookup"><span data-stu-id="6543a-1824">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="6543a-1825">針對 ADF V2 資料流程偵錯工作階段新增動作命令：Start-AzDataFactoryV2DataFlowDebugSession、Get-AzDataFactoryV2DataFlowDebugSession、Add-AzDataFactoryV2DataFlowDebugSessionPackage、Invoke-AzDataFactoryV2DataFlowDebugSessionCommand 和 Stop-AzDataFactoryV2DataFlowDebugSession。</span><span class="sxs-lookup"><span data-stu-id="6543a-1825">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="6543a-1826">將 ADF .Net SDK 版本更新為 4.2.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1826">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-1827">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-1827">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-1828">修正帳戶驗證，以便在沒有網域的情況下傳遞具有 '-' 的帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-1828">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="6543a-1829">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="6543a-1829">Az.HealthcareApis</span></span>
* <span data-ttu-id="6543a-1830">已將 Powershell 版本更新為 1.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1830">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="6543a-1831">已將 SDK 版本更新為 1.0.2</span><span class="sxs-lookup"><span data-stu-id="6543a-1831">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="6543a-1832">更新測試以參考新的 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-1832">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="6543a-1833">已將輸出結構從巢狀更新為壓平合併。</span><span class="sxs-lookup"><span data-stu-id="6543a-1833">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1834">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1835">新增新的路由來源：DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="6543a-1835">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="6543a-1836">次要錯誤修正：Get-AzIothub 未傳回 subscriptionId</span><span class="sxs-lookup"><span data-stu-id="6543a-1836">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1837">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1837">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1838">已針對動作群組新增新的動作群組接收器   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="6543a-1838">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="6543a-1839">針對接收器使用已啟用的一般警示結構描述。</span><span class="sxs-lookup"><span data-stu-id="6543a-1839">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="6543a-1840">這不適用於 SMS、Azure App 撨送、ITSM 和 Voice 接收器</span><span class="sxs-lookup"><span data-stu-id="6543a-1840">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="6543a-1841">Webhooks 現在支援 Azure Active Directory 驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-1841">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1842">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1842">Az.Network</span></span>
* <span data-ttu-id="6543a-1843">新增新的 Cmdlet Get-AzAvailableServiceAlias 以便進行呼叫並取得可用於服務端點原則的別名。</span><span class="sxs-lookup"><span data-stu-id="6543a-1843">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="6543a-1844">已在虛擬網路閘道連線新增了流量選取器的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1844">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="6543a-1845">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1845">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-1846">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-1846">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="6543a-1847">已更新選用參數的 Cmdlet -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1847">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6543a-1848">新增網路安全性規則組態中針對 ESP 和 AH 通訊協定的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1848">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="6543a-1849">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1849">Updated cmdlets:</span></span>
        - <span data-ttu-id="6543a-1850">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1850">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6543a-1851">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1851">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6543a-1852">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-1852">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6543a-1853">改善 Cortex Cmdlet 中的例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="6543a-1853">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="6543a-1854">適用於 VirtualNetworkGateways 的新項目和 SKU</span><span class="sxs-lookup"><span data-stu-id="6543a-1854">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="6543a-1855">引進新一代的 VirtualNetworkGateways。</span><span class="sxs-lookup"><span data-stu-id="6543a-1855">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="6543a-1856">引進適用於 VirtualNetworkGateways 的全新高輸送量 SKU。</span><span class="sxs-lookup"><span data-stu-id="6543a-1856">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6543a-1857">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6543a-1857">Az.RedisCache</span></span>
* <span data-ttu-id="6543a-1858">更新了 'Set-AzRedisCache' 參考文件，納入了 '-Size' 參數缺少的值</span><span class="sxs-lookup"><span data-stu-id="6543a-1858">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1859">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1859">Az.Sql</span></span>
* <span data-ttu-id="6543a-1860">新增在受控執行個體上設定 Active Directory 系統管理員的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-1860">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1861">Az.Storage</span></span>
* <span data-ttu-id="6543a-1862">將儲存體用戶端程式庫升級為 11.1.0</span><span class="sxs-lookup"><span data-stu-id="6543a-1862">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="6543a-1863">列出具有管理平面 API 的容器，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="6543a-1863">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6543a-1864">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6543a-1864">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="6543a-1865">列出訂用帳戶中的儲存體帳戶，將會以 NextPageLink 列出</span><span class="sxs-lookup"><span data-stu-id="6543a-1865">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="6543a-1866">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-1866">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6543a-1867">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6543a-1867">Az.StorageSync</span></span>
* <span data-ttu-id="6543a-1868">修正 Reset-AzStorageSyncServerCertificate 中的問題 9810。</span><span class="sxs-lookup"><span data-stu-id="6543a-1868">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1869">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1869">Az.Websites</span></span>
* <span data-ttu-id="6543a-1870">Set-AzWebApp 更新應用程式的 ASP 時失敗</span><span class="sxs-lookup"><span data-stu-id="6543a-1870">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="6543a-1871">2.7.0 - 2019 年 9 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1871">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6543a-1872">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-1872">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-1873">更新 'Set-AzApiManagementPolicy' 參考文件中的 '-Format' 參數描述</span><span class="sxs-lookup"><span data-stu-id="6543a-1873">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="6543a-1874">已移除參考文件中的 'Update-AzApiManagementDeployment' 參考，此 Cmdlet 已被取代。</span><span class="sxs-lookup"><span data-stu-id="6543a-1874">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="6543a-1875">改為使用 'Set-AzApiManagement'。</span><span class="sxs-lookup"><span data-stu-id="6543a-1875">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-1876">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-1876">Az.Automation</span></span>
* <span data-ttu-id="6543a-1877">已修正 'Register-AzAutomationDscNode' 參考文件中範例的錯別字</span><span class="sxs-lookup"><span data-stu-id="6543a-1877">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="6543a-1878">已新增 Register-AzAutomationDSCNode 的 OS 限制說明</span><span class="sxs-lookup"><span data-stu-id="6543a-1878">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="6543a-1879">已針對 -Wait 選項修正了 Start-AzAutomationRunbook Cmdlet 的 Null 參考例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6543a-1879">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-1880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-1880">Az.Compute</span></span>
* <span data-ttu-id="6543a-1881">在 New-AzDiskConfig 中新增 UploadSizeInBytes 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1881">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="6543a-1882">在 New-AzSnapshotConfig 中新增增量參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1882">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6543a-1883">新增低優先順序虛擬機器功能：</span><span class="sxs-lookup"><span data-stu-id="6543a-1883">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="6543a-1884">已將 MaxPrice、EvictionPolicy 和 Priority 參數新增到 New-AzVMConfig。</span><span class="sxs-lookup"><span data-stu-id="6543a-1884">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="6543a-1885">已將 MaxPrice 參數新增到 New-AzVmssConfig、Update-AzVM 和 Update-AzVmss Cmdlet 中。</span><span class="sxs-lookup"><span data-stu-id="6543a-1885">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="6543a-1886">修正 Get-AzAvailabilitySet Cmdlet 的參考問題，以免在訂用帳戶中列出所有可用性設定組。</span><span class="sxs-lookup"><span data-stu-id="6543a-1886">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="6543a-1887">修正 Get-AzRemoteDesktopFile 的 Null 例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6543a-1887">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="6543a-1888">修正適用於端點相關位置的 VHD Seek 方法。</span><span class="sxs-lookup"><span data-stu-id="6543a-1888">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="6543a-1889">修正 New-AzVM 和 Update-AzVM 的 UltraSSD 問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1889">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-1890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-1890">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-1891">為 ADF V2 新增 3 個新命令 - Add-AzDataFactoryV2TriggerSubscription、Remove-AzDataFactoryV2TriggerSubscription 和 Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="6543a-1891">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="6543a-1892">已將 ADF .Net SDK 版本更新為 4.1.3</span><span class="sxs-lookup"><span data-stu-id="6543a-1892">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-1893">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-1893">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-1894">呼叫重大變更</span><span class="sxs-lookup"><span data-stu-id="6543a-1894">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-1895">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-1895">Az.IotHub</span></span>
* <span data-ttu-id="6543a-1896">針對異地配對災害復原區域新增叫用 IotHub 容錯移轉的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1896">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="6543a-1897">新增管理 IotHub 訊息擴充的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-1897">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="6543a-1898">這些新 Cmdlet 包括：</span><span class="sxs-lookup"><span data-stu-id="6543a-1898">New cmdlets are:</span></span>
    - <span data-ttu-id="6543a-1899">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6543a-1899">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6543a-1900">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6543a-1900">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6543a-1901">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6543a-1901">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="6543a-1902">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="6543a-1902">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-1903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-1903">Az.Monitor</span></span>
* <span data-ttu-id="6543a-1904">指向最近的監視 SDK，例如 0.24.1-preview</span><span class="sxs-lookup"><span data-stu-id="6543a-1904">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="6543a-1905">在 Metrics Cmdlet 中新增不會造成中斷的變更，例如單位列舉支援數個新值。</span><span class="sxs-lookup"><span data-stu-id="6543a-1905">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="6543a-1906">這些 Cmdlet 是唯讀的，因此 Cmdlet 的輸出中不會有任何變更。</span><span class="sxs-lookup"><span data-stu-id="6543a-1906">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="6543a-1907">**ActionGroups** 要求的 api-version 現在為 **2019-06-01** ，之前為 **2018-03-01** 。</span><span class="sxs-lookup"><span data-stu-id="6543a-1907">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="6543a-1908">已針對此項變更新增多個案例測試。</span><span class="sxs-lookup"><span data-stu-id="6543a-1908">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="6543a-1909">**EmailReceiver** 和 **WebhookReceiver** 類別的建構函式新增了一個新的強制引數，例如稱為 **useCommonAlertSchema** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="6543a-1909">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="6543a-1910">目前，該值已修正為 **false** 以隱藏 Cmdlet 的重大變更。</span><span class="sxs-lookup"><span data-stu-id="6543a-1910">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="6543a-1911">**注意** ：這是暫時性的變更，必須由警示小組驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-1911">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="6543a-1912">**Source** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-1912">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6543a-1913">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="6543a-1913">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="6543a-1914">**AlertingAction** 類別之建構函式的引數順序 (與 **ScheduledQueryRuleSource** 類別相關) 已變更，不再是先前的 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-1914">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="6543a-1915">此變更需要修正兩個單元測試：這兩個單元已進行編譯，但無法通過測試。</span><span class="sxs-lookup"><span data-stu-id="6543a-1915">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="6543a-1916">適用於計量警示 V2 的支援動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6543a-1916">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="6543a-1917">New-AzMetricAlertRuleV2Criteria：目前也建立動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6543a-1917">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="6543a-1918">Add-AzMetricAlertRuleV2：目前也接受動態閾值準則</span><span class="sxs-lookup"><span data-stu-id="6543a-1918">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="6543a-1919">已排程查詢規則 Cmdlet (SQR) 中的改善項目</span><span class="sxs-lookup"><span data-stu-id="6543a-1919">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="6543a-1920">Cmdlets 接受兩種格式的 'Location' 參數，包含位置 (例如 eastus) 或位置顯示名稱 (例如美國東部)</span><span class="sxs-lookup"><span data-stu-id="6543a-1920">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="6543a-1921">在說明檔案中適當地描述 ’Enabled’ 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-1921">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="6543a-1922">已新增 'ActionGroup' 選用參數的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1922">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="6543a-1923">說明檔內容全面改善</span><span class="sxs-lookup"><span data-stu-id="6543a-1923">Overall improved help files</span></span>
* <span data-ttu-id="6543a-1924">修正判斷 'Set-AzActionRule' 範圍類型的錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-1924">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-1925">Az.Network</span></span>
* <span data-ttu-id="6543a-1926">修正 'New-AzApplicationGateway' 參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1926">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="6543a-1927">在 'Get-AzNetworkWatcherPacketCapture' 參考文件中新增註解，說明擷取封包取得之所有屬性的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-1927">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="6543a-1928">已修正 'Test-AzNetworkWatcherIPFlow' 參考文件中的範例，以便正確地列舉 NIC</span><span class="sxs-lookup"><span data-stu-id="6543a-1928">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="6543a-1929">改善了雲端例外狀況剖析，以便顯示其他詳細資料 (若有)</span><span class="sxs-lookup"><span data-stu-id="6543a-1929">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="6543a-1930">改善了雲端例外狀況剖析，以便處理 SDK 例外狀況的其他類型</span><span class="sxs-lookup"><span data-stu-id="6543a-1930">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="6543a-1931">修正了不正確的安全性規則模型對應</span><span class="sxs-lookup"><span data-stu-id="6543a-1931">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="6543a-1932">在網路介面中新增了屬性以提供 IP 功能</span><span class="sxs-lookup"><span data-stu-id="6543a-1932">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="6543a-1933">在 PSNetworkInterface 中新增了 'PrivateEndpoint' 屬性作為 PSResourceId 類型</span><span class="sxs-lookup"><span data-stu-id="6543a-1933">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="6543a-1934">在 PSNetworkInterfaceIPConfiguration 中新增了 'PrivateLinkConnectionProperties' 屬性作為 PSIpConfigurationConnectivityInformation 類型</span><span class="sxs-lookup"><span data-stu-id="6543a-1934">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="6543a-1935">新增了模型類別 PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="6543a-1935">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="6543a-1936">針對 Azure 防火牆資源新增了 ApplicationRuleProtocolType 'mssql'</span><span class="sxs-lookup"><span data-stu-id="6543a-1936">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="6543a-1937">在虛擬 WAN 中支援多連結</span><span class="sxs-lookup"><span data-stu-id="6543a-1937">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="6543a-1938">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1938">New cmdlets</span></span>
        - <span data-ttu-id="6543a-1939">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="6543a-1939">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="6543a-1940">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1940">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="6543a-1941">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-1941">Updated cmdlet:</span></span>
        - <span data-ttu-id="6543a-1942">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6543a-1942">New-VpnSite</span></span>
        - <span data-ttu-id="6543a-1943">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="6543a-1943">Update-VpnSite</span></span>
        - <span data-ttu-id="6543a-1944">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1944">New-VpnConnection</span></span>
        - <span data-ttu-id="6543a-1945">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-1945">Update-VpnConnection</span></span>
* <span data-ttu-id="6543a-1946">修正了文件中的部分 PowerShell 範例，改為使用 Az Cmdlet 而非 AzureRM Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1946">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-1947">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-1947">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-1948">透過 ProtectedItemsCount 屬性更新 AzureVMpolicy 物件</span><span class="sxs-lookup"><span data-stu-id="6543a-1948">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="6543a-1949">新增了 VM 原則和原始儲存體帳戶還原的測試</span><span class="sxs-lookup"><span data-stu-id="6543a-1949">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-1950">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-1950">Az.Resources</span></span>
* <span data-ttu-id="6543a-1951">修正無法在沒有參數範圍的情況下呼叫 New-AzRoleAssignment 的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1951">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-1952">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-1952">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-1953">修正了 'Update-AzServiceFabricReliability' 參考文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-1953">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="6543a-1954">新增 Cmdlet 以管理應用程式和服務：</span><span class="sxs-lookup"><span data-stu-id="6543a-1954">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="6543a-1955">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6543a-1955">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6543a-1956">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6543a-1956">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6543a-1957">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6543a-1957">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6543a-1958">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6543a-1958">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="6543a-1959">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6543a-1959">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6543a-1960">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6543a-1960">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6543a-1961">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6543a-1961">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6543a-1962">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6543a-1962">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6543a-1963">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6543a-1963">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="6543a-1964">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="6543a-1964">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="6543a-1965">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="6543a-1965">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="6543a-1966">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="6543a-1966">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="6543a-1967">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="6543a-1967">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="6543a-1968">已將 Service Fabric SDK 更新為版本 1.2.0，此版本使用服務網狀架構資源提供者 api-version 2019-03-01。</span><span class="sxs-lookup"><span data-stu-id="6543a-1968">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6543a-1969">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6543a-1969">Az.SignalR</span></span>
* <span data-ttu-id="6543a-1970">新增 Update、Restart、CheckNameAvailability、GetUsage 等 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-1970">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-1971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-1971">Az.Sql</span></span>
* <span data-ttu-id="6543a-1972">更新 'Get-AzSqlElasticPool' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1972">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="6543a-1973">新增了虛擬核心範例以建立彈性集區 (New-AzSqlElasticPool)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1973">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="6543a-1974">移除 EmailAddresses 的驗證，並確認 Set-AzSqlServerAdvancedThreatProtectionPolicy 和 Set-AzSqlDatabaseAdvancedThreatProtectionPolicy 中的 EmailAdmins 為空的情況下 EmailAdmins 的狀態並非 false</span><span class="sxs-lookup"><span data-stu-id="6543a-1974">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="6543a-1975">當多個啟用稽核分類的診斷設定存在時，啟用了伺服器/資料庫稽核設定的移除功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-1975">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="6543a-1976">修正多個 Sql 弱點評估 Cmdlet 中的電子郵件地址驗證 (Update-AzSqlDatabaseVulnerabilityAssessmentSetting、Update-AzSqlServerVulnerabilityAssessmentSetting、Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting 和 Update-AzSqlInstanceVulnerabilityAssessmentSetting)。</span><span class="sxs-lookup"><span data-stu-id="6543a-1976">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-1977">Az.Storage</span></span>
* <span data-ttu-id="6543a-1978">已更新 'Get-AzStorageAccountKey' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1978">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="6543a-1979">在上傳/下載 Azure 檔案中，支援保留目的地檔案中的來源檔案 SMB 屬性 (檔案屬性、檔案建立時間、檔案最後入時間)</span><span class="sxs-lookup"><span data-stu-id="6543a-1979">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="6543a-1980">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6543a-1980">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="6543a-1981">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6543a-1981">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="6543a-1982">修正上傳區塊 Blob 的屬性/metadate 在啟用 ImmutabilityPolicy 的容器中失敗的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-1982">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="6543a-1983">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6543a-1983">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="6543a-1984">支援透過管理平面 API 管理 Azure 檔案共用</span><span class="sxs-lookup"><span data-stu-id="6543a-1984">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="6543a-1985">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1985">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6543a-1986">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1986">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6543a-1987">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1987">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="6543a-1988">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6543a-1988">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-1989">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-1989">Az.Websites</span></span>
* <span data-ttu-id="6543a-1990">修正將應用程式遷移到新的 ASP 時系統會刪除 webapp 標籤的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1990">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="6543a-1991">修正 Publish-AzureWebapp 以在 Linux 和 Windows 上運作</span><span class="sxs-lookup"><span data-stu-id="6543a-1991">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="6543a-1992">更新 'Get-AzWebAppPublishingProfile' 參考文件中的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-1992">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="6543a-1993">2.6.0 - 2019 年 8 月</span><span class="sxs-lookup"><span data-stu-id="6543a-1993">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="6543a-1994">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-1994">General</span></span>
* <span data-ttu-id="6543a-1995">修正了多個模組中的各種錯字問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1995">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-1996">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-1996">Az.Accounts</span></span>
* <span data-ttu-id="6543a-1997">支援 Azure Functions 驗證中使用者指派的 MSI (#9479)</span><span class="sxs-lookup"><span data-stu-id="6543a-1997">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-1998">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-1998">Az.Aks</span></span>
* <span data-ttu-id="6543a-1999">修正 'Get-AzAks' 的輸出問題</span><span class="sxs-lookup"><span data-stu-id="6543a-1999">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="6543a-2000">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="6543a-2000">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-2001">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-2001">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-2002">修正 https://github.com/Azure/azure-powershell/issues/9351 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2002">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="6543a-2003">更新 .Net NuGet 版本，此版本不會強制執行 productId、apiId、groupId 和 userId 的限制</span><span class="sxs-lookup"><span data-stu-id="6543a-2003">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="6543a-2004">**Get-AzApiManagementProduct** - 新增了使用 API 查詢產品的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2004">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="6543a-2005">**New-AzApiManagementApiRevision** - 修正在建立新 API 版本時並未設定 ApiRevisionDescription 的問題 https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="6543a-2005">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="6543a-2006">將模型 'PsApiManagementOAuth2AuthrozationServer' 中的錯字修正為 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6543a-2006">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-2007">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-2007">Az.Batch</span></span>
* <span data-ttu-id="6543a-2008">修正了說明訊息和文件中的錯字，將 Windows 首字變大寫</span><span class="sxs-lookup"><span data-stu-id="6543a-2008">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-2009">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-2009">Az.Cdn</span></span>
* <span data-ttu-id="6543a-2010">修正了 CDN 模組轉換協助程式中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2010">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2011">Az.Compute</span></span>
* <span data-ttu-id="6543a-2012">將 VmssId 新增到 New-AzVMConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2012">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="6543a-2013">將 TerminateScheduledEvents 和 TerminateScheduledEventNotBeforeTimeoutInMinutes 參數新增到 New-AzVmssConfig 和 Update-AzVmss 中</span><span class="sxs-lookup"><span data-stu-id="6543a-2013">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="6543a-2014">將 HyperVGeneration 屬性新增到 VM 映像物件中</span><span class="sxs-lookup"><span data-stu-id="6543a-2014">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="6543a-2015">新增 Host 和 HostGroup 功能</span><span class="sxs-lookup"><span data-stu-id="6543a-2015">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="6543a-2016">新的 Cmdlet： New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6543a-2016">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="6543a-2017">已將 HostId 參數新增到 New-AzVMConfig 和 New-AzVM 中</span><span class="sxs-lookup"><span data-stu-id="6543a-2017">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="6543a-2018">更新 'Invoke-AzVMRunCommand' 文件中的範例，使用了正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2018">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="6543a-2019">更新 'Set-AzVMDiskEncryptionExtension' 和 'Set-AzVmssDiskEncryptionExtension' 參考文件中的 '-VolumeType' 描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2019">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2020">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2020">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2021">修正錯字，將 'New-AzDataFactoryEncryptValue' 文件中的 'Windows' 變成首字大寫</span><span class="sxs-lookup"><span data-stu-id="6543a-2021">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="6543a-2022">已將 ADF .Net SDK 版本更新為 4.1.2</span><span class="sxs-lookup"><span data-stu-id="6543a-2022">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="6543a-2023">對 'Set-AzureRmDataFactoryV2IntegrationRuntime' Cmd 新增參數 'DataProxyIntegrationRuntimeName'、'DataProxyStagingLinkedServiceName' 和 'DataProxyStagingPath'，以將自我裝載整合執行階段設定為適用於 SSIS 整合執行階段的 Proxy</span><span class="sxs-lookup"><span data-stu-id="6543a-2023">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="6543a-2024">更新了 PSTriggerRun 以顯示觸發的管線、訊息、屬性和 PSActivityRun，以顯示活動類型</span><span class="sxs-lookup"><span data-stu-id="6543a-2024">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2025">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2025">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2026">修正 Get-DataLakeStoreDeletedItem 凸排的問題，避免產生任何錯誤或遠端例外狀況。</span><span class="sxs-lookup"><span data-stu-id="6543a-2026">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-2027">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2027">Az.EventHub</span></span>
* <span data-ttu-id="6543a-2028">修正 #9658 的問題：Set-AzEventHubNetworkRuleSet 中 VirtualNteworkRule 參數的錯字問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2028">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="6543a-2029">修正 #9558 的問題：Set-AzEventHubNamespace 使用 PATCH 而非 PUT</span><span class="sxs-lookup"><span data-stu-id="6543a-2029">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="6543a-2030">已將 EnableKafka 參數新增到 Set-AzEventHubNamespace Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2030">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="6543a-2031">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="6543a-2031">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="6543a-2032">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6543a-2032">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6543a-2033">修正了文件中 'Azure'均為小寫的錯字問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2033">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-2034">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2034">Az.Monitor</span></span>
* <span data-ttu-id="6543a-2035">已修正說明文件中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2035">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2036">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2036">Az.Network</span></span>
* <span data-ttu-id="6543a-2037">更新了 New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2037">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="6543a-2038">取代了 'PublicIpAddress' 參數，因為伺服器端從未使用過此參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2038">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="6543a-2039">新增了選用參數 'Primary'，指出正確的 IP 設定是否為主要。</span><span class="sxs-lookup"><span data-stu-id="6543a-2039">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="6543a-2040">改善了 SDK 要求錯誤例外狀況的處理方式 - 修正了之前未正確處理的 SDK 例外狀況而導致金鑰錯誤詳細資料並未顯示的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2040">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="6543a-2041">調整了 Ipv6 IP 首碼的驗證邏輯，以便檢查正確的 IPv6 前置長度。</span><span class="sxs-lookup"><span data-stu-id="6543a-2041">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="6543a-2042">更新了 Get-AzVirtualNetworkSubnetConfig：依子網路 ID 新增了要取得的參數集。</span><span class="sxs-lookup"><span data-stu-id="6543a-2042">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="6543a-2043">對 AzNetworkServiceTag 新增位置參數的描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2043">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2045">更新了 'New-AzOperationalInsightsLinuxSyslogDataSource' 文件</span><span class="sxs-lookup"><span data-stu-id="6543a-2045">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="6543a-2046">新增了範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2046">Added example</span></span>
    - <span data-ttu-id="6543a-2047">更新了 '-Name' 參數的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2047">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="6543a-2048">新增了 New-AzOperationalInsightsWindowsEventDataSource 的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2048">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="6543a-2049">對 New-AzOperationalInsightsWindowsEventDataSource 變更了 -Name 參數的描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2049">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2050">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2050">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2051">更新 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2051">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2052">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2052">Az.Resources</span></span>
* <span data-ttu-id="6543a-2053">新增對於 Microsoft.Resource 新 API 版本 2019-05-10 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2053">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="6543a-2054">新增對 'copy.count = 0' 中的變數、資源和屬性的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2054">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="6543a-2055">完整模式中將會刪除具有 'condition = false' 或 'copy.count = 0' 的資源</span><span class="sxs-lookup"><span data-stu-id="6543a-2055">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="6543a-2056">在說明文件的訂閱層級中新增了指派原則範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2056">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-2057">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-2057">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-2058">修正 #9658 的問題：Set-AzServiceBusNetworkRuleSet 中 VirtualNetworkRule 參數的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2058">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="6543a-2059">修正 #9786 的問題：無法建立僅限接聽權限的規則</span><span class="sxs-lookup"><span data-stu-id="6543a-2059">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="6543a-2060">新增了 'Test-AzServiceBusNameAvailability' 命令以檢查佇列和主題的名稱可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-2060">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-2061">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-2061">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-2062">修正新增節點類型 Cmdlet 錯誤 (bug)：</span><span class="sxs-lookup"><span data-stu-id="6543a-2062">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="6543a-2063">當資源群組具有其他與服務網狀架構叢集不相關之 vmss 時的 NullReferenceException 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2063">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="6543a-2064">修正問題： https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="6543a-2064">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="6543a-2065">修正若 virtualNetwork 在與叢集不同的資源群組中時 Cmdlet 會失敗的錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2065">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="6543a-2066">修正問題： https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="6543a-2066">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="6543a-2067">取代 Add-AzServiceFabricApplicationCertificate Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2067">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2068">Az.Sql</span></span>
* <span data-ttu-id="6543a-2069">更新舊版 Auditing Cmdlet 文件。</span><span class="sxs-lookup"><span data-stu-id="6543a-2069">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2070">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2070">Az.Storage</span></span>
* <span data-ttu-id="6543a-2071">更新 Get/Close-AzStorageFileHandle 的說明，在 Cmdlet 範例中新增更多案例並更新參數描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2071">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="6543a-2072">支援上傳 Blob 和複製 Blob 中的 StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6543a-2072">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="6543a-2073">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6543a-2073">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="6543a-2074">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6543a-2074">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="6543a-2075">支援複製 Blob 中的 Rehydrate Priority</span><span class="sxs-lookup"><span data-stu-id="6543a-2075">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="6543a-2076">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6543a-2076">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2077">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2077">Az.Websites</span></span>
* <span data-ttu-id="6543a-2078">釐清 Set-AzWebApp 和 Set-AzWebAppSlot 中的 -AppSettings 參數的</span><span class="sxs-lookup"><span data-stu-id="6543a-2078">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="6543a-2079">2.5.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2079">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2080">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2080">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2081">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6543a-2081">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="6543a-2082">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2082">Az.ApplicationInsights</span></span>
* <span data-ttu-id="6543a-2083">修正 'Remove-AzApplicationInsightsApiKey' 文件中範例的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2083">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2084">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2084">Az.Automation</span></span>
* <span data-ttu-id="6543a-2085">修正資源字串中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2085">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-2086">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2086">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-2087">新增了 NetworkRuleSet 支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2087">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2088">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2088">Az.Compute</span></span>
* <span data-ttu-id="6543a-2089">新增 虛擬機器執行個體檢視物件缺少的屬性 (ComputerName、OsName、OsVersion 和 HyperVGeneration)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2089">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6543a-2090">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6543a-2090">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6543a-2091">修正 Replication 參數的 Remove-AzContainerRegistryReplication 中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2091">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="6543a-2092">如需詳細資訊，請參閱 https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="6543a-2092">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2093">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2094">已將 ADF .Net SDK 版本更新為 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6543a-2094">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="6543a-2095">修正 'Get-AzDataFactoryV2PipelineRun' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2095">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-2096">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2096">Az.EventHub</span></span>
* <span data-ttu-id="6543a-2097">新增了 Cmmdlet 以產生 SAS 權杖：New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6543a-2097">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6543a-2098">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-2098">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-2099">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2099">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-2100">新增了為憑證原則指定 KeySize 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2100">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6543a-2101">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6543a-2101">Az.LogicApp</span></span>
* <span data-ttu-id="6543a-2102">修正 Get-AzIntegrationAccountMap 以列出所有對應類型</span><span class="sxs-lookup"><span data-stu-id="6543a-2102">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="6543a-2103">新增了用於篩選的 MapType 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2103">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="6543a-2104">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2104">Az.ManagedServices</span></span>
* <span data-ttu-id="6543a-2105">新增了 API 版本 2019-06-01 (GA) 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2105">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2106">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2106">Az.Network</span></span>
* <span data-ttu-id="6543a-2107">新增私人端點和私人連結服務的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2107">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="6543a-2108">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2108">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2109">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6543a-2109">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6543a-2110">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2110">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6543a-2111">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2111">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-2112">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2112">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-2113">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2113">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-2114">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2114">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="6543a-2115">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="6543a-2115">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="6543a-2116">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2116">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="6543a-2117">已更新下列功能命令：Virtualnetwork 中子網路上的 PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies 旗標</span><span class="sxs-lookup"><span data-stu-id="6543a-2117">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="6543a-2118">更新了 New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2118">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="6543a-2119">新增了選用參數 -PrivateEndpointNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人端點網路原則。</span><span class="sxs-lookup"><span data-stu-id="6543a-2119">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="6543a-2120">新增了選用參數 -PrivateLinkServiceNetworkPoliciesFlag，此參數會設定是否要套用此子網路中的私人連結服務網路原則。</span><span class="sxs-lookup"><span data-stu-id="6543a-2120">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="6543a-2121">AzPrivateLinkService 的 Cmdlet 參數 'ServiceName' 已更名為 'Name' 搭配別名 'ServiceName' 以提供回溯相容性</span><span class="sxs-lookup"><span data-stu-id="6543a-2121">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="6543a-2122">針對網路安全性規則組態啟用 ICMP 通訊協定</span><span class="sxs-lookup"><span data-stu-id="6543a-2122">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="6543a-2123">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2123">Updated cmdlets</span></span>
        - <span data-ttu-id="6543a-2124">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2124">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6543a-2125">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2125">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="6543a-2126">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2126">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="6543a-2127">新增 ConnectionProtocolType (Ikev1/Ikev2) 作為 New-AzVirtualNetworkGatewayConnection 的可設定參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2127">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="6543a-2128">在 LoadBalancerFrontendIpConfiguration 中新增 PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="6543a-2128">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="6543a-2129">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2129">Updated cmdlet:</span></span>
        - <span data-ttu-id="6543a-2130">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2130">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6543a-2131">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2131">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="6543a-2132">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2132">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="6543a-2133">更新應用程式閘道 New-AzApplicationGatewayProbeConfig 命令以支援探查中的自訂連接埠</span><span class="sxs-lookup"><span data-stu-id="6543a-2133">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="6543a-2134">更新了 New-AzApplicationGatewayProbeConfig：新增了用來探查後端伺服器的選用參數 Port。</span><span class="sxs-lookup"><span data-stu-id="6543a-2134">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="6543a-2135">此參數適用於 Standard_V2 和 WAF_V2 SKU。</span><span class="sxs-lookup"><span data-stu-id="6543a-2135">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2136">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2136">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2137">更新了預設版本，讓已儲存的搜尋為 1。</span><span class="sxs-lookup"><span data-stu-id="6543a-2137">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="6543a-2138">修正了自訂記錄 Null 處理</span><span class="sxs-lookup"><span data-stu-id="6543a-2138">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2139">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2139">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2140">更新 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2140">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6543a-2141">更新 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2141">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="6543a-2142">更新 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2142">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="6543a-2143">更新 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2143">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="6543a-2144">更新 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2144">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="6543a-2145">更新 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2145">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6543a-2146">更新 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2146">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="6543a-2147">更新 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2147">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="6543a-2148">針對 Azure File Share 的 Unregistering 容器更新了服務呼叫</span><span class="sxs-lookup"><span data-stu-id="6543a-2148">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="6543a-2149">更新 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="6543a-2149">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2150">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2150">Az.Resources</span></span>
- <span data-ttu-id="6543a-2151">移除 'New-AzResourceGroupDeployment' 文件中參考的遺漏 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2151">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="6543a-2152">更新原則 Cmdlet 以使用新的 API 版本 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="6543a-2152">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-2153">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-2153">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-2154">新增了 Cmmdlet 以產生 SAS 權杖：New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="6543a-2154">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="6543a-2155">在只有已指派 'Manage' 的情況下，新增了 authorizationrules 權限的驗證和錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-2155">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2156">Az.Sql</span></span>
* <span data-ttu-id="6543a-2157">修正 Set-AzSqlDatabaseSecondary Cmdlet 遺漏的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2157">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="6543a-2158">修正集合弱點評量期性掃描並未提供任何電子郵件地址的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2158">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="6543a-2159">修正警告訊息中的錯字。</span><span class="sxs-lookup"><span data-stu-id="6543a-2159">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2160">Az.Storage</span></span>
* <span data-ttu-id="6543a-2161">更新 'Get-AzStorageAccount' 參考文件中的範例，以使用正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2161">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6543a-2162">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6543a-2162">Az.StorageSync</span></span>
* <span data-ttu-id="6543a-2163">新增 Invoke-AzStorageSyncChangeDetection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-2163">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="6543a-2164">修正問題 9551 以接受 TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="6543a-2164">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2165">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2165">Az.Websites</span></span>
* <span data-ttu-id="6543a-2166">修正 Get-AzWebApp 和 Set-AzWebApp 並未傳回部分 SiteConfig 屬性的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-2166">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="6543a-2167">新增 Get-AzDeletedWebApp 和 Restore-AzDeletedWebApp 的位置參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2167">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="6543a-2168">修正 New-AzWebApp -IncludeSourceWebAppSlots 複製 Web 應用程式的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-2168">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="6543a-2169">2.4.0 - 2019 年 7 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2169">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2170">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2170">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2171">新增設定檔 Cmdlet 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2171">Add support for profile cmdlets</span></span>
* <span data-ttu-id="6543a-2172">在產生的 Cmdlet 中新增環境和資料平面的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2172">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="6543a-2173">修正以下錯誤，在 Windows PowerShell 中不正確的端點在某些情況下用於資料平面 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2173">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="6543a-2174">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="6543a-2174">Az.Advisor</span></span>
* <span data-ttu-id="6543a-2175">Az.Advisor 的 GA 版本</span><span class="sxs-lookup"><span data-stu-id="6543a-2175">GA release of Az.Advisor</span></span>
* <span data-ttu-id="6543a-2176">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="6543a-2176">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="6543a-2177">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-2177">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-2178">修正 https://github.com/Azure/azure-powershell/issues/8671 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2178">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="6543a-2179">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6543a-2179">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="6543a-2180">新增了依使用者和產品查詢訂用帳戶的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2180">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="6543a-2181">新增了使用 Scope '/'、'/apis'、'/apis/echo-api' 進行查詢的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2181">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="6543a-2182">修正 https://github.com/Azure/azure-powershell/issues/9307 和 https://github.com/Azure/azure-powershell/issues/8432 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2182">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="6543a-2183">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6543a-2183">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="6543a-2184">新增了可在匯入 Api 時指定 'ApiVersion' 和 'ApiVersionSetId' 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2184">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2185">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2185">Az.Automation</span></span>
* <span data-ttu-id="6543a-2186">修正了 Set-AzAutomationConnectionFieldValue Cmdlet 錯誤以處理字串值。</span><span class="sxs-lookup"><span data-stu-id="6543a-2186">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2187">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2187">Az.Compute</span></span>
* <span data-ttu-id="6543a-2188">將 HyperVGeneration 參數新增到 New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2188">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2189">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2190">更新取得活動執行、取得管線執行和取得觸發程序執行 ADF Cmdlet 的輸出，以支援 Select-Object 管道。</span><span class="sxs-lookup"><span data-stu-id="6543a-2190">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6543a-2191">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6543a-2191">Az.EventGrid</span></span>
* <span data-ttu-id="6543a-2192">修正 'New-AzEventGridSubscription' 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2192">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-2193">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2193">Az.IotHub</span></span>
* <span data-ttu-id="6543a-2194">新增對重新產生授權原則金鑰的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2194">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2195">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2195">Az.Network</span></span>
* <span data-ttu-id="6543a-2196">已將 'RoutingPreference' 新增到公用 ip 標籤</span><span class="sxs-lookup"><span data-stu-id="6543a-2196">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="6543a-2197">改善 'Get-AzNetworkServiceTag' 參考文件的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2197">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-2198">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2198">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-2199">修正 Get-AzPolicyState 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2199">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="6543a-2200">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="6543a-2200">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2201">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2201">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2202">修正了 Get-AzOperationalInsightsDataSource 中傳回的 CustomLog 資料來源模型</span><span class="sxs-lookup"><span data-stu-id="6543a-2202">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2203">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2203">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2204">修正 IaaSVM 的 get-policy 命令</span><span class="sxs-lookup"><span data-stu-id="6543a-2204">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2205">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2205">Az.Resources</span></span>
    - <span data-ttu-id="6543a-2206">修正 Get-AzPolicyState -Top 參數的說明文字</span><span class="sxs-lookup"><span data-stu-id="6543a-2206">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="6543a-2207">新增 Get-AzPolicyAlias 的用戶端分頁支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2207">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="6543a-2208">新增 Set-AzPolicyAssignment、-PolicyParameters 和 -PolicyParametersObject 的新參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2208">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="6543a-2209">原則 Cmdlet 的幾個文件與範例更新</span><span class="sxs-lookup"><span data-stu-id="6543a-2209">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-2210">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-2210">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-2211">修正問題 #4938 - 設定 MaxSizeInMegabytes 時，New-AzureRmServiceBusQueue 傳回 BadRequest</span><span class="sxs-lookup"><span data-stu-id="6543a-2211">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2212">Az.Sql</span></span>
* <span data-ttu-id="6543a-2213">從預覽版本新增執行個體容錯移轉群組 Cmdlet 至公用版本</span><span class="sxs-lookup"><span data-stu-id="6543a-2213">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="6543a-2214">支援使用新的 Cmdlet 進行 Azure SQL Server\資料庫稽核。</span><span class="sxs-lookup"><span data-stu-id="6543a-2214">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="6543a-2215">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2215">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6543a-2216">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2216">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6543a-2217">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2217">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="6543a-2218">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2218">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6543a-2219">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2219">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="6543a-2220">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6543a-2220">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="6543a-2221">從弱點評量設定移除電子郵件條件約束</span><span class="sxs-lookup"><span data-stu-id="6543a-2221">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2222">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2222">Az.Storage</span></span>
* <span data-ttu-id="6543a-2223">在 Cmdlet 中將 2 個參數 '-IndexDocument' 和 '-ErrorDocument404Path' 從必要變更為選用：</span><span class="sxs-lookup"><span data-stu-id="6543a-2223">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="6543a-2224">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6543a-2224">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="6543a-2225">藉新增範例更新 Get-AzStorageBlobContent 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2225">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="6543a-2226">當 Cmdlet 失敗並出現 StorageException 時顯示錯誤詳細資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-2226">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="6543a-2227">支援使用 Azure 檔案 AAD DS 驗證建立或更新儲存體帳戶</span><span class="sxs-lookup"><span data-stu-id="6543a-2227">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="6543a-2228">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2228">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="6543a-2229">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2229">Set-AzStorageAccount</span></span>
* <span data-ttu-id="6543a-2230">支援清單或關閉檔案共用、檔案目錄或檔案的檔案控制代碼</span><span class="sxs-lookup"><span data-stu-id="6543a-2230">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="6543a-2231">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6543a-2231">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="6543a-2232">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="6543a-2232">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="6543a-2233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="6543a-2233">Az.StorageSync</span></span>
* <span data-ttu-id="6543a-2234">此模組現包含為彙總 `Az` 模組的一部分</span><span class="sxs-lookup"><span data-stu-id="6543a-2234">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="6543a-2235">2.3.2 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2235">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2236">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2236">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2237">修正函式呼叫時在某些情況下使用了不正確 URL 的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-2237">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="6543a-2238">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="6543a-2238">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="6543a-2239">修正從 AzureRM 到 Az Cmdlet 的別名問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2239">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="6543a-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6543a-2240">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="6543a-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="6543a-2241">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2242">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2242">Az.Compute</span></span>
* <span data-ttu-id="6543a-2243">New-AzVm and New-AzVmss 簡單參數集合現在接受 'ProximityPlacementGroup' 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2243">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="6543a-2244">修正 'New-AzVM' 參考文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2244">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="6543a-2245">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6543a-2245">Az.Dns</span></span>
* <span data-ttu-id="6543a-2246">修正了 'Set-AzDnsZone' 說明範例中的錯字。</span><span class="sxs-lookup"><span data-stu-id="6543a-2246">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6543a-2247">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6543a-2247">Az.EventGrid</span></span>
* <span data-ttu-id="6543a-2248">已更新為使用 2019-06-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6543a-2248">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="6543a-2249">新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2249">New cmdlets:</span></span>
    - <span data-ttu-id="6543a-2250">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6543a-2250">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6543a-2251">建立新的 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="6543a-2251">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6543a-2252">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6543a-2252">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6543a-2253">取得事件方格網域的詳細資料，或取得目前 Azure 訂用帳戶中的所有事件方格網域清單。</span><span class="sxs-lookup"><span data-stu-id="6543a-2253">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="6543a-2254">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="6543a-2254">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="6543a-2255">移除 Azure 事件方格網域。</span><span class="sxs-lookup"><span data-stu-id="6543a-2255">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6543a-2256">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6543a-2256">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6543a-2257">重新產生 Azure 事件方格網域適用的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="6543a-2257">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="6543a-2258">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="6543a-2258">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="6543a-2259">取得用來; 事件發佈至事件方格網域的共用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="6543a-2259">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="6543a-2260">New-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="6543a-2260">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6543a-2261">建立新的 Azure事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2261">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="6543a-2262">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="6543a-2262">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="6543a-2263">取得事件方格網域主題的詳細資料，或取得目前 Azure 中特定事件方格網域下的所有事件方格網域主題清單</span><span class="sxs-lookup"><span data-stu-id="6543a-2263">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="6543a-2264">Remove-AzureRmEventGridDomainTopic：</span><span class="sxs-lookup"><span data-stu-id="6543a-2264">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="6543a-2265">移除現有的 Azure 事件方格網域主題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2265">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="6543a-2266">已更新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2266">Updated cmdlets:</span></span>
    - <span data-ttu-id="6543a-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="6543a-2267">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="6543a-2268">新增新的必要參數，以支援新的事件方格網域和事件方格網域主題管線，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6543a-2268">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6543a-2269">新增新的必要參數，以指定新的事件方格網域名稱和/或事件方格網域主題名稱，並允許在這些資源下建立新的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6543a-2269">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="6543a-2270">為網域和網域主題新增新的參數集合，以允許重新使用現有的參數 (例如 EndPointType、SubjectBeginsWith 等)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2270">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="6543a-2271">新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6543a-2271">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="6543a-2272">事件訂用帳戶過期日期，</span><span class="sxs-lookup"><span data-stu-id="6543a-2272">Event subscription expiration date,</span></span>
            - <span data-ttu-id="6543a-2273">進階篩選參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2273">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="6543a-2274">為 servicebusqueue 新增新的列舉成為目的地。</span><span class="sxs-lookup"><span data-stu-id="6543a-2274">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="6543a-2275">不允許使用 'All' in -IncludedEventType 選項並取代為</span><span class="sxs-lookup"><span data-stu-id="6543a-2275">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="6543a-2276">Get-AzEventGridTopic、Get-AzEventGridDomain、Get-AzEventGridDomainTopic、Get-AzEventGridSubscription：</span><span class="sxs-lookup"><span data-stu-id="6543a-2276">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="6543a-2277">新增新的選用參數 (Top、ODataQuery 和 NextLink) 以支援結果分頁和篩選條件。</span><span class="sxs-lookup"><span data-stu-id="6543a-2277">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="6543a-2278">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="6543a-2278">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="6543a-2279">新增新的必要參數，以支援事件方格網域和事件方格網域主題管線，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6543a-2279">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="6543a-2280">新增新的必要參數，以指定事件方格網域名稱和/或事件方格網域主題名稱，並允許移除這些資源下現有的事件訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="6543a-2280">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-2281">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-2281">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-2282">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="6543a-2282">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="6543a-2283">新增轉換支援和新的運算子自動完成值 (RegEx)</span><span class="sxs-lookup"><span data-stu-id="6543a-2283">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="6543a-2284">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="6543a-2284">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="6543a-2285">新增新的自動完成值</span><span class="sxs-lookup"><span data-stu-id="6543a-2285">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2286">Az.Network</span></span>
* <span data-ttu-id="6543a-2287">新增對虛擬網路閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2287">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="6543a-2288">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2288">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="6543a-2289">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="6543a-2290">新增 AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6543a-2290">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="6543a-2291">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2291">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2292">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6543a-2292">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="6543a-2293">新增 PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2293">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="6543a-2294">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2294">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2295">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2295">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6543a-2296">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2296">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6543a-2297">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="6543a-2297">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="6543a-2298">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2298">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="6543a-2299">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2299">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="6543a-2300">新增 PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6543a-2300">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="6543a-2301">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2301">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2302">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6543a-2302">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6543a-2303">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6543a-2303">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6543a-2304">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="6543a-2304">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="6543a-2305">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="6543a-2305">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="6543a-2306">已更新下列功能命令：VpnConnection 上的 UseLocalAzureIpAddress 旗標</span><span class="sxs-lookup"><span data-stu-id="6543a-2306">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="6543a-2307">更新了 New-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="6543a-2307">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="6543a-2308">更新了 Set-AzVpnConnection：新增了選用的參數 -UseLocalAzureIpAddress 以在開始連線時，指示應該使用本機 Azure Ip 位址作為來源位址。</span><span class="sxs-lookup"><span data-stu-id="6543a-2308">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="6543a-2309">在 ExpressRoute 對等互連中新增了唯讀欄位 PeeredConnections。</span><span class="sxs-lookup"><span data-stu-id="6543a-2309">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="6543a-2310">在 ExpressRoute 中新增了唯讀欄位 GlobalReachEnabled。</span><span class="sxs-lookup"><span data-stu-id="6543a-2310">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="6543a-2311">新增了重大變更屬性以取消取代 ExpressRouteCircuit 模型中的 AllowGlobalReach 欄位</span><span class="sxs-lookup"><span data-stu-id="6543a-2311">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="6543a-2312">修正了使用 TargetListenerID 搭配 AzApplicationGatewayRedirectConfiguration Cmdlet 的問題 8756 錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-2312">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="6543a-2313">修正了 New-AzApplicationGatewayPathRuleConfig 中的錯誤，防止進行重寫規則集合設定。</span><span class="sxs-lookup"><span data-stu-id="6543a-2313">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="6543a-2314">修正了在 NetworkInterfaceIpConfiguration 中顯示 VirtualNetworkTaps 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2314">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="6543a-2315">修正了 Cortex Get Cmdlet 以列出所有部分</span><span class="sxs-lookup"><span data-stu-id="6543a-2315">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="6543a-2316">修正了 ExpressRouteGateways 和 VpnGatewayVirtualHub 的參考建立</span><span class="sxs-lookup"><span data-stu-id="6543a-2316">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="6543a-2317">新增了 AzureFirewall 和 NatGateway 中對可用性區域的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2317">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="6543a-2318">新增了 Cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="6543a-2318">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="6543a-2319">新增針對 Azure 防火牆的多個公用 IP 位址的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2319">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="6543a-2320">更新了 New-AzFirewall Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2320">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="6543a-2321">新增了參數 -PublicIpAddress 以接受一或多個 Public IP Address 物件</span><span class="sxs-lookup"><span data-stu-id="6543a-2321">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="6543a-2322">新增了參數 -VirtualNetwork 以接受虛擬網路物件</span><span class="sxs-lookup"><span data-stu-id="6543a-2322">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="6543a-2323">在防火牆物件中新增了 AddPublicIpAddress 和 RemovePublicIpAddress 方法 - 以接受 Public IP Address 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="6543a-2323">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="6543a-2324">參數 -PublicIpName 和 -VirtualNetworkName 已被取代</span><span class="sxs-lookup"><span data-stu-id="6543a-2324">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="6543a-2325">已更新下列功能命令：將 VpnClient AAD 驗證選項設為虛擬網路閘道資源。</span><span class="sxs-lookup"><span data-stu-id="6543a-2325">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="6543a-2326">已更新 New-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6543a-2326">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6543a-2327">已更新 Set-AzVirtualNetworkGateway：新增了選用參數 AadTenantUri,AadAudienceId,AadIssuerUri 以在閘道上設定 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6543a-2327">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="6543a-2328">已更新 Set-AzVirtualNetworkGateway：新增了選用的切換參數 RemoveAadAuthentication 以從閘道移除 VpnClient AAD 驗證選項。</span><span class="sxs-lookup"><span data-stu-id="6543a-2328">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2329">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2329">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2330">在 'New-AzureRmOperationalInsightsWorkspace' 命令中啟用 **pergb2018** 定價層</span><span class="sxs-lookup"><span data-stu-id="6543a-2330">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2331">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2331">Az.Resources</span></span>
* <span data-ttu-id="6543a-2332">支援其他範本匯出選項</span><span class="sxs-lookup"><span data-stu-id="6543a-2332">Support for additional Template Export options</span></span>
    - <span data-ttu-id="6543a-2333">將 '-SkipResourceNameParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-2333">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6543a-2334">將 '-SkipAllParameterization' 參數新增到 Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-2334">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="6543a-2335">將 '-Resource' parameter 新增到 Export-AzResourceGroup 以篩選已匯出的資源</span><span class="sxs-lookup"><span data-stu-id="6543a-2335">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-2336">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-2336">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-2337">修正在某些情況下，新增 ByExistingKeyVault 憑證會產生錯誤指紋的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2337">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2338">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2338">Az.Sql</span></span>
* <span data-ttu-id="6543a-2339">修正進階威脅防護儲存體端點尾碼</span><span class="sxs-lookup"><span data-stu-id="6543a-2339">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="6543a-2340">修正進階威脅防護啟用覆寫進階威脅防護原則</span><span class="sxs-lookup"><span data-stu-id="6543a-2340">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="6543a-2341">為 Management.Sql 新增 Cmdlet 以允許客戶為受控執行個體新增 TDE 金鑰並設定 TDE 保護程式</span><span class="sxs-lookup"><span data-stu-id="6543a-2341">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="6543a-2342">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6543a-2342">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6543a-2343">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6543a-2343">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6543a-2344">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6543a-2344">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="6543a-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6543a-2345">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="6543a-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6543a-2346">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2347">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2347">Az.Storage</span></span>
* <span data-ttu-id="6543a-2348">在建立儲體帳戶時支援 Kind FileStorage 和 SkuName Premium_ZRS</span><span class="sxs-lookup"><span data-stu-id="6543a-2348">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="6543a-2349">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2349">New-AzStorageAccount</span></span>
* <span data-ttu-id="6543a-2350">釐清了 Blob 不變性 Cmdlet 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2350">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="6543a-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2351">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2352">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2352">Az.Websites</span></span>
* <span data-ttu-id="6543a-2353">將 Get-AzWebAppCertificate 最佳化，以便依伺服器而非用戶端上的資源群組篩選</span><span class="sxs-lookup"><span data-stu-id="6543a-2353">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="6543a-2354">將 -UseDisasterRecovery 切換參數新增到 Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6543a-2354">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="6543a-2355">2.2.0 - 2019 年 6 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2355">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="6543a-2356">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-2356">Az.Cdn</span></span>
* <span data-ttu-id="6543a-2357">已更新 Cmdlet，可支援以 API 2019-04-15 版為基礎的 rulesEngine 功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-2357">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2358">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2358">Az.Compute</span></span>
* <span data-ttu-id="6543a-2359">已新增 `NoWait` 參數，會啟動作業並在作業完成之前立即傳回結果。</span><span class="sxs-lookup"><span data-stu-id="6543a-2359">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="6543a-2360">已更新的 Cmdlet： Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6543a-2360">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-2361">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2361">Az.EventHub</span></span>
* <span data-ttu-id="6543a-2362">修正 #9231 - Get-AzEventHubNamespace 不會傳回標記</span><span class="sxs-lookup"><span data-stu-id="6543a-2362">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="6543a-2363">修正 #9230 - Get-AzEventHubNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6543a-2363">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2364">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2364">Az.Network</span></span>
* <span data-ttu-id="6543a-2365">更新 Nat 閘道的 ResourceId 和 InputObject</span><span class="sxs-lookup"><span data-stu-id="6543a-2365">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="6543a-2366">新增 ResourceId 和 InputObject 的別名</span><span class="sxs-lookup"><span data-stu-id="6543a-2366">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-2367">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2367">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-2368">修正 Get-AzPolicyEvent 中的 Null 參考問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2368">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2369">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2370">IaaSVM 原則的最小保留天數從 1 天變更為 7 天</span><span class="sxs-lookup"><span data-stu-id="6543a-2370">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-2371">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-2371">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-2372">修正 issue #9182 - Get-AzServiceBusNamespace 會傳回 ResourceGroup，而非 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6543a-2372">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-2373">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-2373">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-2374">修正 'Update-AzServiceFabricReliability' 錯誤訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2374">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="6543a-2375">修正 Service Fabric 命令列中的遺漏字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2375">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2376">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2376">Az.Sql</span></span>
* <span data-ttu-id="6543a-2377">為 New-AzureSqlInstance Cmdlet 新增 DnsZonePartner 參數，以支援受控執行個體的 AutoDr。</span><span class="sxs-lookup"><span data-stu-id="6543a-2377">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="6543a-2378">即將淘汰 Get-AzSqlDatabaseSecureConnectionPolicy Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2378">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="6543a-2379">將威脅偵測 Cmdlet 重新命名為進階威脅防護</span><span class="sxs-lookup"><span data-stu-id="6543a-2379">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="6543a-2380">New-AzSqlInstance -StorageSizeInGB 和 -LicenseType 現在是選擇性的參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2380">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2381">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2381">Az.Websites</span></span>
* <span data-ttu-id="6543a-2382">修正 Set-AzWebApp 和 Set-AzWebAppSlot 搭配使用 -WebApp 屬性時會移除標記的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2382">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="6543a-2383">2.1.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2383">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="6543a-2384">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-2384">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-2385">已建立新的 Cmdlet，用以管理全域和 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="6543a-2385">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="6543a-2386">**Get-AzApiManagementDiagnostic** - 取得設定於全域或 API 範圍的診斷</span><span class="sxs-lookup"><span data-stu-id="6543a-2386">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="6543a-2387">**New-AzApiManagementDiagnostic** - 在全域範圍或 API 範圍建立新的診斷</span><span class="sxs-lookup"><span data-stu-id="6543a-2387">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="6543a-2388">**New-AzApiManagementHttpMessageDiagnostic** - 建立關於要記錄哪些標頭和本文位元組大小的診斷設定</span><span class="sxs-lookup"><span data-stu-id="6543a-2388">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="6543a-2389">**New-AzApiManagementPipelineDiagnosticSetting** - 建立閘道的傳入/傳出 HTTP 訊息的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="6543a-2389">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="6543a-2390">**New-AzApiManagementSamplingSetting** - 建立診斷要求/回應的取樣設定</span><span class="sxs-lookup"><span data-stu-id="6543a-2390">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="6543a-2391">**Remove-AzApiManagementDiagnostic** - 移除全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="6543a-2391">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="6543a-2392">**Set-AzApiManagementDiagnostic** - 更新全域或 API 範圍的診斷實體</span><span class="sxs-lookup"><span data-stu-id="6543a-2392">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="6543a-2393">已建立新的 Cmdlet 用以管理 ApiManagement 服務中的快取</span><span class="sxs-lookup"><span data-stu-id="6543a-2393">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="6543a-2394">**Get-AzApiManagementCache** - 取得識別碼所指定的快取或所有快取的詳細資料</span><span class="sxs-lookup"><span data-stu-id="6543a-2394">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="6543a-2395">**New-AzApiManagementCache** - 建立新的「預設」快取或特定 Azure「區域」中的快取</span><span class="sxs-lookup"><span data-stu-id="6543a-2395">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="6543a-2396">**Remove-AzApiManagementCache** - 移除快取</span><span class="sxs-lookup"><span data-stu-id="6543a-2396">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="6543a-2397">**Update-AzApiManagementCache** - 更新快取</span><span class="sxs-lookup"><span data-stu-id="6543a-2397">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="6543a-2398">已建立新的 Cmdlet 用以管理 API 結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2398">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="6543a-2399">**New-AzApiManagementSchema** - 為 API 建立新的結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2399">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="6543a-2400">**Get-AzApiManagementSchema** - 取得在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2400">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="6543a-2401">**Remove-AzApiManagementSchema** - 移除在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2401">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="6543a-2402">**Set-AzApiManagementSchema** - 更新在 API 中設定的結構描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2402">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="6543a-2403">已建立新的 Cmdlet 用以產生使用者權杖。</span><span class="sxs-lookup"><span data-stu-id="6543a-2403">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="6543a-2404">**New-AzApiManagementUserToken** - 產生預設有效期為 8 小時的新使用者權杖。'GIT' 使用者的權杖可使用此 Cmdlet 產生。/</span><span class="sxs-lookup"><span data-stu-id="6543a-2404">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="6543a-2405">已建立新的 Cmdlet 用以擷取網路狀態</span><span class="sxs-lookup"><span data-stu-id="6543a-2405">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="6543a-2406">**Get-AzApiManagementNetworkStatus** - 取得 API 管理服務相依資源的網路狀態連線。</span><span class="sxs-lookup"><span data-stu-id="6543a-2406">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="6543a-2407">這在將 ApiManagement 服務部署到虛擬網路和驗證是否有任何相依性中斷時，將可發揮效用。</span><span class="sxs-lookup"><span data-stu-id="6543a-2407">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="6543a-2408">已更新 Cmdlet **New-AzApiManagement** ，用以管理 ApiManagement 服務</span><span class="sxs-lookup"><span data-stu-id="6543a-2408">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="6543a-2409">已加入新的「使用量」SKU 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2409">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="6543a-2410">已加入為「使用量」SKU 開啟 'EnableClientCertificate' 旗標的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2410">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="6543a-2411">新的 Cmdlet **New-AzApiManagementSslSetting** 允許在「後端」和「前端」設定 'TLS/SSL' 設定。</span><span class="sxs-lookup"><span data-stu-id="6543a-2411">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="6543a-2412">這也可用來在 ApiManagement 服務的「前端」設定「編碼器」 (例如 '3DES') 和 'ServerProtocols' (例如 'Http2')。</span><span class="sxs-lookup"><span data-stu-id="6543a-2412">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="6543a-2413">已加入在 ApiManagement 服務上設定 'DeveloperPortal' 主機名稱的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2413">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="6543a-2414">已更新 Cmdlet **Get-AzApiManagementSsoToken** ，以使用 'PsApiManagement' 物件作為輸入</span><span class="sxs-lookup"><span data-stu-id="6543a-2414">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="6543a-2415">已更新 Cmdlet 以顯示內嵌錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-2415">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="6543a-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy :錯誤碼：ValidationError 錯誤訊息：有一或多個欄位包含不正確的值：錯誤詳細資料：[Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10:Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="6543a-2416">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="6543a-2417">已更新 Cmdlet **Export-AzApiManagementApi** ，以採用 'OpenApi 3.0' 格式匯出 API</span><span class="sxs-lookup"><span data-stu-id="6543a-2417">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="6543a-2418">已更新 Cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6543a-2418">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6543a-2419">以從 'OpenApi 3.0' 文件規格匯入 API</span><span class="sxs-lookup"><span data-stu-id="6543a-2419">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="6543a-2420">以覆寫任何 ('Swagger'、'Wadl'、'Wsdl'、'OpenApi') 文件中指定的 'PsApiManagementSchema' 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-2420">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="6543a-2421">以覆寫任何文件中指定的 'ServiceUrl' 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-2421">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="6543a-2422">已更新 Cmdlet **Get-AzApiManagementPolicy** ，以透過使用 'rawxml' 的非 XML 逸出「格式」傳回原則</span><span class="sxs-lookup"><span data-stu-id="6543a-2422">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="6543a-2423">已更新 Cmdlet **Set-AzApiManagementPolicy** ，以接受使用 'rawxml' 的非 XML 逸出「格式」和使用 'xml' 溢出的 XML 格式的原則</span><span class="sxs-lookup"><span data-stu-id="6543a-2423">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="6543a-2424">已更新 Cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6543a-2424">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6543a-2425">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="6543a-2425">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6543a-2426">以在 'ApiVersionSet' 中建立 API</span><span class="sxs-lookup"><span data-stu-id="6543a-2426">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6543a-2427">以使用 'SourceApiId' 和 'SourceApiRevision' 複製 API。</span><span class="sxs-lookup"><span data-stu-id="6543a-2427">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="6543a-2428">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="6543a-2428">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6543a-2429">已更新 Cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="6543a-2429">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="6543a-2430">以透過 'OpenId' 授權伺服器設定 API。</span><span class="sxs-lookup"><span data-stu-id="6543a-2430">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="6543a-2431">以在 'ApiVersionSet' 中更新 API</span><span class="sxs-lookup"><span data-stu-id="6543a-2431">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="6543a-2432">能夠在 API 範圍設定 'SubscriptionRequired'。</span><span class="sxs-lookup"><span data-stu-id="6543a-2432">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="6543a-2433">已更新 Cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="6543a-2433">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="6543a-2434">以使用 'SourceApiRevision' 複製 (複製標記、產品、作業和原則) 現有的修訂。</span><span class="sxs-lookup"><span data-stu-id="6543a-2434">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="6543a-2435">新的修訂會採用父代的 'ApiId'。</span><span class="sxs-lookup"><span data-stu-id="6543a-2435">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="6543a-2436">以提供 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="6543a-2436">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="6543a-2437">以在複製 API 時覆寫 'ServiceUrl'。</span><span class="sxs-lookup"><span data-stu-id="6543a-2437">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="6543a-2438">已更新 Cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="6543a-2438">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="6543a-2439">以透過 'Authority' 設定 'AAD' 或 'AADB2C'</span><span class="sxs-lookup"><span data-stu-id="6543a-2439">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="6543a-2440">以設定 'SignupPolicy'、'SigninPolicy'、'ProfileEditingPolicy' 和 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="6543a-2440">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="6543a-2441">已更新 Cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6543a-2441">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6543a-2442">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="6543a-2442">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6543a-2443">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="6543a-2443">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6543a-2444">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2444">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6543a-2445">已更新 Cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="6543a-2445">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="6543a-2446">以使用 'Scope' 和 'UserId' 說明新的 SubscriptonModel</span><span class="sxs-lookup"><span data-stu-id="6543a-2446">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="6543a-2447">以使用 'ProductId' 和 'UserId' 說明舊的訂用帳戶模型</span><span class="sxs-lookup"><span data-stu-id="6543a-2447">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="6543a-2448">加入在訂用帳戶層級啟用 'AllowTracing' 的支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2448">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="6543a-2449">已更新下列 Cmdlet，以接受 'ResourceId' 作為輸入</span><span class="sxs-lookup"><span data-stu-id="6543a-2449">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="6543a-2450">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="6543a-2450">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="6543a-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="6543a-2451">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="6543a-2452">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="6543a-2452">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="6543a-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="6543a-2453">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="6543a-2454">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6543a-2454">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="6543a-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="6543a-2455">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="6543a-2456">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="6543a-2456">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="6543a-2457">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="6543a-2457">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="6543a-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="6543a-2458">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="6543a-2459">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="6543a-2459">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="6543a-2460">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="6543a-2460">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="6543a-2461">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="6543a-2461">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2462">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2462">Az.Automation</span></span>
* <span data-ttu-id="6543a-2463">已更新 Get-AzAutomationJobOutputRecord 以處理 JSON 和文字記錄值。</span><span class="sxs-lookup"><span data-stu-id="6543a-2463">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="6543a-2464">修正 https://github.com/Azure/azure-powershell/issues/7977 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2464">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="6543a-2465">修正 https://github.com/Azure/azure-powershell/issues/8600 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2465">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="6543a-2466">已將 Start-AzAutomationDscCompilationJob 的行為變更為僅啟動作業而不等候作業完成。</span><span class="sxs-lookup"><span data-stu-id="6543a-2466">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="6543a-2467">修正 https://github.com/Azure/azure-powershell/issues/8347 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2467">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="6543a-2468">修正 Get-AzAutomationDscNode 在使用 -Name 時會傳回所有節點的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2468">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="6543a-2469">現在它只會相符的節點。</span><span class="sxs-lookup"><span data-stu-id="6543a-2469">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2470">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2470">Az.Compute</span></span>
* <span data-ttu-id="6543a-2471">將 ProtectFromScaleIn 和 ProtectFromScaleSetAction 參數新增至 Update-AzVmssVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-2471">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="6543a-2472">在不支援「美國東部」時，New-AzVM wimple 參數現在依預設會使用可用的位置</span><span class="sxs-lookup"><span data-stu-id="6543a-2472">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2473">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2473">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2474">更新 ADLS SDK 以使用 httpclient，並透過 Azure 架構整合資料平面測試</span><span class="sxs-lookup"><span data-stu-id="6543a-2474">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-2475">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2475">Az.Monitor</span></span>
* <span data-ttu-id="6543a-2476">已修正說明範例中不正確的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2476">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2477">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2477">Az.Network</span></span>
* <span data-ttu-id="6543a-2478">將 DisableBgpRoutePropagation 旗標新增至有效路由表輸出</span><span class="sxs-lookup"><span data-stu-id="6543a-2478">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="6543a-2479">已更新 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2479">Updated cmdlet:</span></span>
        - <span data-ttu-id="6543a-2480">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-2480">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="6543a-2481">修正 New-AzApplicationGatewayTrustedRootCertificate 文件中的雙破折號</span><span class="sxs-lookup"><span data-stu-id="6543a-2481">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2482">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2482">Az.Resources</span></span>
* <span data-ttu-id="6543a-2483">新增 Cmdlet Get-AzureRmDenyAssignment 用以擷取拒絕指派</span><span class="sxs-lookup"><span data-stu-id="6543a-2483">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2484">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2484">Az.Sql</span></span>
* <span data-ttu-id="6543a-2485">將進階威脅防護 Cmdlet 重新命名為進階資料安全性的，並依預設啟用弱點評量</span><span class="sxs-lookup"><span data-stu-id="6543a-2485">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="6543a-2486">2.0.0 - 2019 年 5 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2486">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2487">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2487">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2488">更新驗證程式庫以修正 ADFS 的使用者名稱/密碼驗證問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2488">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-2489">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2489">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-2490">只顯示 Bing 搜尋服務的 Bing 免責聲明。</span><span class="sxs-lookup"><span data-stu-id="6543a-2490">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="6543a-2491">改善建立帳戶失敗時的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-2491">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2492">Az.Compute</span></span>
* <span data-ttu-id="6543a-2493">鄰近放置群組功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-2493">Proximity placement group feature.</span></span>
    - <span data-ttu-id="6543a-2494">新增下列 Cmdlet： New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-2494">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="6543a-2495">將新參數 ProximityPlacementGroupId 新增至下列 Cmdlet： New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2495">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="6543a-2496">將 StorageAccountType 參數新增至 New-AzGalleryImageVersion。</span><span class="sxs-lookup"><span data-stu-id="6543a-2496">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="6543a-2497">New-AzGalleryImageVersion 的 TargetRegion 可包含 StorageAccountType。</span><span class="sxs-lookup"><span data-stu-id="6543a-2497">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="6543a-2498">將 SkipShutdown 切換參數新增至 Stop-AzVM 和 Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6543a-2498">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="6543a-2499">重大變更</span><span class="sxs-lookup"><span data-stu-id="6543a-2499">Breaking changes</span></span>
    - <span data-ttu-id="6543a-2500">將 Set-AzVMBootDiagnostics 變更為 Set-AzVMBootDiagnostic。</span><span class="sxs-lookup"><span data-stu-id="6543a-2500">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="6543a-2501">將 Export-AzLogAnalyticThrottledRequests 變更為 Export-AzLogAnalyticThrottledRequests。</span><span class="sxs-lookup"><span data-stu-id="6543a-2501">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="6543a-2502">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="6543a-2502">Az.DeploymentManager</span></span>
* <span data-ttu-id="6543a-2503">第一版正式運作的 Azure 部署管理員 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2503">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="6543a-2504">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="6543a-2504">Az.Dns</span></span>
* <span data-ttu-id="6543a-2505">自動的 DNS NameServer 委派</span><span class="sxs-lookup"><span data-stu-id="6543a-2505">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="6543a-2506">建立 DNS 區域 Cmdlet 可接受父代區域名稱作為其他選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2506">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="6543a-2507">針對新建立的子系區域，在父代區域中新增 NS 記錄。</span><span class="sxs-lookup"><span data-stu-id="6543a-2507">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="6543a-2508">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-2508">Az.FrontDoor</span></span>
* <span data-ttu-id="6543a-2509">第一版正式運作的 Azure FrontDoor Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2509">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="6543a-2510">重新命名 WAF Cmdlet 以包含 'Waf'</span><span class="sxs-lookup"><span data-stu-id="6543a-2510">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="6543a-2511">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-2511">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-2512">移除兩個 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2512">Removed two cmdlets:</span></span>
    - <span data-ttu-id="6543a-2513">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6543a-2513">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="6543a-2514">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6543a-2514">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6543a-2515">已新增 Set-AzHDInsightGatewayCredential Cmdlet 來取代 Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6543a-2515">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="6543a-2516">更新 Get-AzHDInsightJobOutput Cmdlet 以區分讀者角色和 HDInsight 操作員角色：</span><span class="sxs-lookup"><span data-stu-id="6543a-2516">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="6543a-2517">具有讀者角色的使用者必須明確指定 'DefaultStorageAccountKey' 參數，否則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="6543a-2517">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="6543a-2518">具有 HDInsight 操作員角色的使用者不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="6543a-2518">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-2519">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2519">Az.Monitor</span></span>
* <span data-ttu-id="6543a-2520">SQR API 的新 Cmdlet (已排程的查詢規則)</span><span class="sxs-lookup"><span data-stu-id="6543a-2520">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="6543a-2521">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="6543a-2521">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="6543a-2522">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="6543a-2522">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="6543a-2523">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="6543a-2523">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="6543a-2524">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="6543a-2524">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="6543a-2525">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="6543a-2525">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="6543a-2526">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="6543a-2526">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="6543a-2527">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2527">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6543a-2528">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2528">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6543a-2529">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2529">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6543a-2530">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2530">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6543a-2531">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2531">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="6543a-2532">[更多](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) SQR API 的相關資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-2532">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="6543a-2533">更新 Az.Monitor.md，以包含用於 GenV2 (非傳統) 計量式警示規則的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2533">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2534">Az.Network</span></span>
* <span data-ttu-id="6543a-2535">新增 Nat 閘道資源的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2535">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="6543a-2536">新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2536">New cmdlets</span></span>
        - <span data-ttu-id="6543a-2537">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6543a-2537">New-AzNatGateway</span></span>
        - <span data-ttu-id="6543a-2538">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6543a-2538">Get-AzNatGateway</span></span>
        - <span data-ttu-id="6543a-2539">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6543a-2539">Set-AzNatGateway</span></span>
        - <span data-ttu-id="6543a-2540">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6543a-2540">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="6543a-2541">更新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2541">Updated cmdlets</span></span>
        - <span data-ttu-id="6543a-2542">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6543a-2542">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="6543a-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="6543a-2543">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="6543a-2544">已更新下列功能命令：設定/移除 Brooklyn 閘道上的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6543a-2544">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="6543a-2545">已更新 New-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6543a-2545">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="6543a-2546">已更新 Set-AzVirtualNetworkGateway：新增選擇性參數 -CustomRoute，以將位址前置詞設定為閘道上設定的自訂路由。</span><span class="sxs-lookup"><span data-stu-id="6543a-2546">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-2547">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2547">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-2548">支援查詢原則的評估詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6543a-2548">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="6543a-2549">將 '-Expand' 參數新增至 Get-AzPolicyState。</span><span class="sxs-lookup"><span data-stu-id="6543a-2549">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="6543a-2550">支援 '-Expand PolicyEvaluationDetails'。</span><span class="sxs-lookup"><span data-stu-id="6543a-2550">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2551">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2552">支援跨訂用帳戶的 Azure 到 Azure 站台復原。</span><span class="sxs-lookup"><span data-stu-id="6543a-2552">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="6543a-2553">標示 Azure Site Recovery 上即將進行的重大變更。</span><span class="sxs-lookup"><span data-stu-id="6543a-2553">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="6543a-2554">Azure Site Recovery 復原計劃和行動計劃的修正。</span><span class="sxs-lookup"><span data-stu-id="6543a-2554">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="6543a-2555">Azure 到 Azure 的 Azure Site Recovery 更新網路對應修正。</span><span class="sxs-lookup"><span data-stu-id="6543a-2555">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="6543a-2556">受控磁碟中 Azure 到 Azure 的 Azure Site Recovery 更新保護方向修正。</span><span class="sxs-lookup"><span data-stu-id="6543a-2556">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="6543a-2557">其他小幅修正。</span><span class="sxs-lookup"><span data-stu-id="6543a-2557">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="6543a-2558">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6543a-2558">Az.Relay</span></span>
* <span data-ttu-id="6543a-2559">修正客戶訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2559">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-2560">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-2560">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-2561">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2561">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2562">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2562">Az.Storage</span></span>
* <span data-ttu-id="6543a-2563">升級至儲存體用戶端程式庫 10.0.1 (此 SDK 中所有物件的命名空間會從 'Microsoft.WindowsAzure.Storage. *' 變更為 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="6543a-2563">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="6543a-2564">升級至 Microsoft.Azure.Management.Storage 11.0.0，以支援新的 API 版本 2019-04-01。</span><span class="sxs-lookup"><span data-stu-id="6543a-2564">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="6543a-2565">建立儲存體帳戶中的預設儲存體帳戶類型從 'Storage' 變更為 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="6543a-2565">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="6543a-2566">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2566">New-AzStorageAccount</span></span>
* <span data-ttu-id="6543a-2567">藉由加入 '-'，將儲存體帳戶 Cmdlet 輸出 Sku.Name 變成和輸入 SkuName 一致，例如將 'StandardLRS' 變更為 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="6543a-2567">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="6543a-2568">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2568">New-AzStorageAccount</span></span>
    - <span data-ttu-id="6543a-2569">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2569">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="6543a-2570">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2570">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2571">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2571">Az.Websites</span></span>
* <span data-ttu-id="6543a-2572">Get-AzWebApp 傳回的 PSSite 物件現在會設定 'Kind' 屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-2572">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="6543a-2573">Get-AzWebApp\*Metrics 和 Get-AzAppServicePlanMetrics 已標示為淘汰</span><span class="sxs-lookup"><span data-stu-id="6543a-2573">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="6543a-2574">1.8.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2574">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-2575">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-2575">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-2576">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-2576">General availability of `Az` module</span></span>
* <span data-ttu-id="6543a-2577">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6543a-2577">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6543a-2578">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6543a-2578">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6543a-2579">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2579">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6543a-2580">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-2580">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6543a-2581">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2581">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6543a-2582">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2582">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-2583">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2583">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2584">更新 Uninstall-AzureRm 以在 Mac 中正確刪除模組</span><span class="sxs-lookup"><span data-stu-id="6543a-2584">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="6543a-2585">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-2585">Az.Batch</span></span>
* <span data-ttu-id="6543a-2586">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2586">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-2587">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-2587">Az.Cdn</span></span>
* <span data-ttu-id="6543a-2588">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2588">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-2589">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2589">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-2590">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2590">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2591">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2591">Az.Compute</span></span>
* <span data-ttu-id="6543a-2592">如果磁碟的資源識別碼中有小寫資源群組，則修正 AEM 安裝問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2592">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="6543a-2593">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2593">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2594">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2594">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2595">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2596">如果受控整合執行階段的 NodeCount 不是 Null，則新增 SsisProperties。</span><span class="sxs-lookup"><span data-stu-id="6543a-2596">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2597">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2598">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2598">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6543a-2599">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6543a-2599">Az.EventGrid</span></span>
* <span data-ttu-id="6543a-2600">已更新端點的說明文字，指出應該先建立資源，才能使用建立/更新事件訂用帳戶 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-2600">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-2601">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2601">Az.EventHub</span></span>
* <span data-ttu-id="6543a-2602">已針對命名空間的 NetworkRuleSet 新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2602">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="6543a-2603">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="6543a-2603">Az.HDInsight</span></span>
* <span data-ttu-id="6543a-2604">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2604">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-2605">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2605">Az.IotHub</span></span>
* <span data-ttu-id="6543a-2606">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2606">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-2607">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2607">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-2608">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2609">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2609">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="6543a-2610">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6543a-2610">Az.MachineLearning</span></span>
* <span data-ttu-id="6543a-2611">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2611">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="6543a-2612">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6543a-2612">Az.Media</span></span>
* <span data-ttu-id="6543a-2613">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2613">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-2614">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2614">Az.Monitor</span></span>
  * <span data-ttu-id="6543a-2615">適用於 GenV2 (非傳統) 計量型警示規則的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2615">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="6543a-2616">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="6543a-2616">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="6543a-2617">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="6543a-2617">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="6543a-2618">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6543a-2618">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6543a-2619">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6543a-2619">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="6543a-2620">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="6543a-2620">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="6543a-2621">監視器 SDK 已更新為版本 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="6543a-2621">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2622">Az.Network</span></span>
* <span data-ttu-id="6543a-2623">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2623">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2624">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2624">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="6543a-2625">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="6543a-2625">Az.NotificationHubs</span></span>
* <span data-ttu-id="6543a-2626">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2627">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2627">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2628">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="6543a-2629">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="6543a-2629">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="6543a-2630">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2631">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2632">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2632">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2633">已更新 Azure VM 中 SQL 的資料表格式</span><span class="sxs-lookup"><span data-stu-id="6543a-2633">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="6543a-2634">已新增替代方法來擷取 AzureFileShare 中的位置</span><span class="sxs-lookup"><span data-stu-id="6543a-2634">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="6543a-2635">已根據時區更新 SchedulePolicy 物件中的 ScheduleRunDays</span><span class="sxs-lookup"><span data-stu-id="6543a-2635">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6543a-2636">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6543a-2636">Az.RedisCache</span></span>
* <span data-ttu-id="6543a-2637">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2637">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2638">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2638">Az.Resources</span></span>
* <span data-ttu-id="6543a-2639">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2639">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2640">Az.Sql</span></span>
* <span data-ttu-id="6543a-2641">以通用程式碼取代監視器 SDK 的相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-2641">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="6543a-2642">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2642">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2643">已增強多個資料行分類的程序。</span><span class="sxs-lookup"><span data-stu-id="6543a-2643">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="6543a-2644">在來自 Get-AzSqlServerServiceObjective 的回應中包含 sku 屬性 (sku 名稱、系列、容量)，並依預設格式化為資料表。</span><span class="sxs-lookup"><span data-stu-id="6543a-2644">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="6543a-2645">依位置 Get-AzSqlServerServiceObjective 的能力，而區域中不需要預先存在的伺服器。</span><span class="sxs-lookup"><span data-stu-id="6543a-2645">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="6543a-2646">在受控執行個體中支援建立時區參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-2646">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="6543a-2647">修正文件中的萬用字元</span><span class="sxs-lookup"><span data-stu-id="6543a-2647">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2648">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2648">Az.Websites</span></span>
* <span data-ttu-id="6543a-2649">將 Set-AzWebApp 和 Set-AzWebAppSlot 修正為不在執行時移除標記</span><span class="sxs-lookup"><span data-stu-id="6543a-2649">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="6543a-2650">已將 Cmdlet 中的複數名詞更新為單數，並已取代複數名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="6543a-2651">已更新網站 SDK。</span><span class="sxs-lookup"><span data-stu-id="6543a-2651">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="6543a-2652">已從 PSAppServicePlan 中移除 AdminSiteName 屬性。</span><span class="sxs-lookup"><span data-stu-id="6543a-2652">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="6543a-2653">1.7.0 - 2019 年 4 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2653">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-2654">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-2654">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-2655">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-2655">General availability of `Az` module</span></span>
* <span data-ttu-id="6543a-2656">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6543a-2656">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6543a-2657">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6543a-2657">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6543a-2658">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2658">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6543a-2659">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-2659">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6543a-2660">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2660">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6543a-2661">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2661">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="6543a-2662">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2662">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2663">已將 Add-AzEnvironment 和 Set-AzEnvironment 更新為接受 AzureAnalysisServicesEndpointResourceId 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2663">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-2664">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2664">Az.AnalysisServices</span></span>
* <span data-ttu-id="6543a-2665">在 dataplane Cmdlet 中使用 ServiceClient，並移除原始的驗證邏輯</span><span class="sxs-lookup"><span data-stu-id="6543a-2665">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="6543a-2666">讓 Add-AzureASAccount 成為 Connect-AzAccount 的包裝函式，以避免重大變更</span><span class="sxs-lookup"><span data-stu-id="6543a-2666">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2667">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2667">Az.Automation</span></span>
* <span data-ttu-id="6543a-2668">修正 Inclusions 的 New-AzAutomationSoftwareUpdateConfiguration Cmdlet 錯誤 (bug)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2668">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="6543a-2669">現在，IncludedKbNumber 和 IncludedPackageNameMask 參數應會正常運作。</span><span class="sxs-lookup"><span data-stu-id="6543a-2669">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="6543a-2670">修正 Azure 自動化更新管理動態群組的錯誤 (bug)</span><span class="sxs-lookup"><span data-stu-id="6543a-2670">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2671">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2671">Az.Compute</span></span>
* <span data-ttu-id="6543a-2672">將 HyperVGeneration 參數新增至 New-AzDiskConfig 和 New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-2672">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="6543a-2673">允許使用其他租用戶的資源庫映像來建立 VM。</span><span class="sxs-lookup"><span data-stu-id="6543a-2673">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="6543a-2674">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-2674">Az.ContainerInstance</span></span>
* <span data-ttu-id="6543a-2675">已修正 New-AzContainerGroup 的 -Command 參數問題，其加入了尾端空白的引數</span><span class="sxs-lookup"><span data-stu-id="6543a-2675">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2676">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2676">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2677">已將 ADF .Net SDK 版本更新為 3.0.2</span><span class="sxs-lookup"><span data-stu-id="6543a-2677">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="6543a-2678">已透過 RepoConfiguration 相關設定的額外參數來更新 Set-AzDataFactoryV2 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-2678">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2679">Az.Resources</span></span>
* <span data-ttu-id="6543a-2680">改善提供 '-ResourceId' 或 '-ResourceGroupName'、'-Name' 和 '-ResourceType' 參數時，'Get-AzResource' 的提供者處理</span><span class="sxs-lookup"><span data-stu-id="6543a-2680">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="6543a-2681">改善 'Test-AzDeployment' 和 'Test-AzResourceGroupDeployment' 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="6543a-2681">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="6543a-2682">處理部署驗證外擲回的錯誤，並改為將其包含在命令輸出中</span><span class="sxs-lookup"><span data-stu-id="6543a-2682">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="6543a-2683">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6543a-2683">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="6543a-2684">將 '-IgnoreDynamicParameters' 切換參數新增至部署 Cmdlet 的集合，以略過指令碼和作業案例中的提示</span><span class="sxs-lookup"><span data-stu-id="6543a-2684">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="6543a-2685">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="6543a-2685">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2686">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2686">Az.Sql</span></span>
* <span data-ttu-id="6543a-2687">支援資料庫的資料分類。</span><span class="sxs-lookup"><span data-stu-id="6543a-2687">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2688">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2688">Az.Storage</span></span>
* <span data-ttu-id="6543a-2689">報告以參數 -UseConnectedAccount 建立儲存體內容時的詳細錯誤 (未登入 Azure 帳戶)</span><span class="sxs-lookup"><span data-stu-id="6543a-2689">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="6543a-2690">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6543a-2690">New-AzStorageContext</span></span>
* <span data-ttu-id="6543a-2691">支援以管理平面 API 管理指定儲存體帳戶的 Blob 服務屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-2691">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="6543a-2692">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6543a-2692">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6543a-2693">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="6543a-2693">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="6543a-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2694">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="6543a-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2695">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="6543a-2696">Blob 的 -AsJob 支援和檔案上傳及下載 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2696">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="6543a-2697">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6543a-2697">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6543a-2698">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6543a-2698">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="6543a-2699">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6543a-2699">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="6543a-2700">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6543a-2700">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="6543a-2701">1.6.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2701">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="6543a-2702">上次發佈主要版本之後的更新重點</span><span class="sxs-lookup"><span data-stu-id="6543a-2702">Highlights since the last major release</span></span>
* <span data-ttu-id="6543a-2703">`Az` 模組的一般可用性</span><span class="sxs-lookup"><span data-stu-id="6543a-2703">General availability of `Az` module</span></span>
* <span data-ttu-id="6543a-2704">如需 `Az` 模組的詳細資訊，請造訪： https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="6543a-2704">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="6543a-2705">新增的 Location、ResourceGroup 和 ResourceName Completer： https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="6543a-2705">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="6543a-2706">新增了適用於 Az.Compute 和 Az.Network 的 Get Cmdlet 萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2706">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="6543a-2707">新增僅適用於 Windows PowerShell 5.1 的互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-2707">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6543a-2708">新增了 Az.Automation 中 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2708">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="6543a-2709">Az.LogicApp：新增了適用於企業整合帳戶組件和批次組態的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2709">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2710">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2710">Az.Automation</span></span>
* <span data-ttu-id="6543a-2711">Azure 自動化更新管理變更為支援下列各項新功能：</span><span class="sxs-lookup"><span data-stu-id="6543a-2711">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="6543a-2712">動態分組</span><span class="sxs-lookup"><span data-stu-id="6543a-2712">Dynamic grouping</span></span>
    * <span data-ttu-id="6543a-2713">預先貼文指令碼</span><span class="sxs-lookup"><span data-stu-id="6543a-2713">Pre-Post script</span></span>
    * <span data-ttu-id="6543a-2714">重新啟動設定</span><span class="sxs-lookup"><span data-stu-id="6543a-2714">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2715">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2715">Az.Compute</span></span>
* <span data-ttu-id="6543a-2716">修正 Get-AzVmBootDiagnosticsData 中路徑解析的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2716">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="6543a-2717">將計算用戶端程式庫更新為 25.0.0。</span><span class="sxs-lookup"><span data-stu-id="6543a-2717">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-2718">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2718">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-2719">新增了 KeyVault Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2719">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2720">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2720">Az.Network</span></span>
* <span data-ttu-id="6543a-2721">新增適用於 Azure 防火牆的威脅智慧支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2721">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="6543a-2722">新增應用程式閘道防火牆原則頂層資源和自訂規則</span><span class="sxs-lookup"><span data-stu-id="6543a-2722">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2723">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2724">已在 Azure VM 原則中新增了 SnapshotRetentionInDays 以支援 Instant RP</span><span class="sxs-lookup"><span data-stu-id="6543a-2724">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="6543a-2725">新增了取消註冊容器的管道支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2725">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2726">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2726">Az.Resources</span></span>
* <span data-ttu-id="6543a-2727">更新適用於 Get-AzResource 和 Get-AzResourceGroup 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2727">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="6543a-2728">更新在對 ARM 進行一般呼叫時使用的認證</span><span class="sxs-lookup"><span data-stu-id="6543a-2728">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2729">Az.Sql</span></span>
* <span data-ttu-id="6543a-2730">變更了 DetectionType 到 string[] 的威脅偵測 Cmdlet 參數，以便在新增了 DetectionTypes 時具備更進一步的保障，同時支援自動完成功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-2730">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2731">Az.Storage</span></span>
* <span data-ttu-id="6543a-2732">支援儲存體帳戶上的 Get/Set/Remove 管理原則</span><span class="sxs-lookup"><span data-stu-id="6543a-2732">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="6543a-2733">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2733">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6543a-2734">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2734">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6543a-2735">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2735">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="6543a-2736">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="6543a-2736">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="6543a-2737">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="6543a-2737">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="6543a-2738">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="6543a-2738">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2739">Az.Websites</span></span>
* <span data-ttu-id="6543a-2740">修正 ARM 範本錯誤 (bug)，防正使用 'New-AzWebApp -IncludeSourceWebAppSlots' 時發生中斷複製所有位置的情況</span><span class="sxs-lookup"><span data-stu-id="6543a-2740">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="6543a-2741">1.5.0 - 2019 年 3 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2741">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2742">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2742">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2743">新增 'Register-AzModule' 命令以支援 AutoRest 產生的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2743">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="6543a-2744">適用於 Connect-AzAccount 的更新範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2744">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2745">Az.Automation</span></span>
* <span data-ttu-id="6543a-2746">修正了在數個 Azure 自動化 Cmdlet 中擷取某些每月排程時發生的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2746">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="6543a-2747">修正 Get-AzAutomationDscNode 只會傳回前 20 個節點的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2747">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="6543a-2748">現在可以傳回所有節點</span><span class="sxs-lookup"><span data-stu-id="6543a-2748">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-2749">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-2749">Az.Cdn</span></span>
* <span data-ttu-id="6543a-2750">新增了 Enable/Disable Custom Domain Https 的 Powershell Cmdlet 並取代了舊的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2750">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2751">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2751">Az.Compute</span></span>
* <span data-ttu-id="6543a-2752">新增 Get Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2752">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2753">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2753">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2754">已將 ADF .Net SDK 版本更新為 3.0.1</span><span class="sxs-lookup"><span data-stu-id="6543a-2754">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6543a-2755">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6543a-2755">Az.LogicApp</span></span>
* <span data-ttu-id="6543a-2756">修正 ListWorkflows，僅擷取結果的第一頁資料</span><span class="sxs-lookup"><span data-stu-id="6543a-2756">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2757">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2757">Az.Network</span></span>
* <span data-ttu-id="6543a-2758">新增 Network Cmdlet 的萬用字元支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2758">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2759">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2759">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2760">新增了Azure VM 中 SQL 伺服器的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2760">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="6543a-2761">SDK 更新</span><span class="sxs-lookup"><span data-stu-id="6543a-2761">SDK Update</span></span>
* <span data-ttu-id="6543a-2762">移除了 Get-ProtectableItem 中的 VMappContainer 檢查</span><span class="sxs-lookup"><span data-stu-id="6543a-2762">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="6543a-2763">新增了 Get-ProtectableItem 的 Name 和 ServerName 參數</span><span class="sxs-lookup"><span data-stu-id="6543a-2763">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2764">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2764">Az.Resources</span></span>
* <span data-ttu-id="6543a-2765">將 `-TemplateObject` 參數新增至部署 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2765">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="6543a-2766">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="6543a-2766">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="6543a-2767">修正將 `Get-AzResource` 結果輸送至 `Set-AzResource` 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2767">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="6543a-2768">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="6543a-2768">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="6543a-2769">修正在執行 `Set-AzResource` 時 JSON 資料類型變更的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2769">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="6543a-2770">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="6543a-2770">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2771">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2771">Az.Sql</span></span>
* <span data-ttu-id="6543a-2772">更新 AuditingEndpointsCommunicator。</span><span class="sxs-lookup"><span data-stu-id="6543a-2772">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="6543a-2773">修正在建立新診斷設定時邊緣案例的行為。</span><span class="sxs-lookup"><span data-stu-id="6543a-2773">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2774">Az.Storage</span></span>
* <span data-ttu-id="6543a-2775">在建立儲存體帳戶時支援 BlockBlobStorage 種類       - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6543a-2775">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="6543a-2776">1.4.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2776">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-2777">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2777">Az.AnalysisServices</span></span>
* <span data-ttu-id="6543a-2778">即將淘汰 AddAzureASAccount Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2778">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2779">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2779">Az.Automation</span></span>
* <span data-ttu-id="6543a-2780">更新 Import-AzAutomationDscNodeConfiguration 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2780">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="6543a-2781">已將設定名稱驗證新增至 Import-AzAutomationDscConfiguration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2781">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="6543a-2782">已改善 Import-AzAutomationDscConfiguration Cmdlet 的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="6543a-2782">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-2783">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2783">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-2784">已將 CustomSubdomainName 新增為 New-AzCognitiveServicesAccount 的新選擇性參數，用來指定資源的子網域。</span><span class="sxs-lookup"><span data-stu-id="6543a-2784">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2785">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2785">Az.Compute</span></span>
* <span data-ttu-id="6543a-2786">修正識別碼參數集問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2786">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="6543a-2787">如果未提供 Name 參數，更新 Get-AzVMExtension 以列出所有已安裝的延伸模組</span><span class="sxs-lookup"><span data-stu-id="6543a-2787">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="6543a-2788">將標記和 ResourceId 參數新增至 Update-AzImage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2788">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="6543a-2789">沒有執行個體識別碼的 Get-AzVmssVM，和具有 InstanceView 者可以透過執行個體檢視列出 VMSS VM。</span><span class="sxs-lookup"><span data-stu-id="6543a-2789">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2790">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2791">為 ADL 刪除的項目列舉和還原新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2791">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="6543a-2792">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2792">Az.EventHub</span></span>
* <span data-ttu-id="6543a-2793">在 Eventhub 的 CaptureDescription 類別中，已將新的布林值屬性 SkipEmptyArchives 新增至 Skip Empty Archives</span><span class="sxs-lookup"><span data-stu-id="6543a-2793">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-2794">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2794">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-2795">修正 Set-AzKeyVaultSecret 的標記</span><span class="sxs-lookup"><span data-stu-id="6543a-2795">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6543a-2796">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6543a-2796">Az.LogicApp</span></span>
* <span data-ttu-id="6543a-2797">在整合帳戶的基本 sku 新增</span><span class="sxs-lookup"><span data-stu-id="6543a-2797">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="6543a-2798">在 XSLT 2.0、XSLT 3.0 和 Liquid 對應類型中新增</span><span class="sxs-lookup"><span data-stu-id="6543a-2798">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="6543a-2799">整合帳戶組件的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2799">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="6543a-2800">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6543a-2800">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6543a-2801">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6543a-2801">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6543a-2802">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6543a-2802">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="6543a-2803">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6543a-2803">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="6543a-2804">整合帳戶批次設定的新 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2804">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="6543a-2805">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-2805">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6543a-2806">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-2806">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6543a-2807">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-2807">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="6543a-2808">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-2808">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="6543a-2809">將邏輯應用程式 SDK 更新至 4.1.0 版</span><span class="sxs-lookup"><span data-stu-id="6543a-2809">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="6543a-2810">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2810">Az.Monitor</span></span>
* <span data-ttu-id="6543a-2811">更新 Get-AzMetric 的說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2811">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2812">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2812">Az.Network</span></span>
* <span data-ttu-id="6543a-2813">更新 Add-AzApplicationGatewayCustomError 的說明範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2813">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-2814">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-2814">Az.OperationalInsights</span></span>
* <span data-ttu-id="6543a-2815">取得 ApplicationInsights 與新資料來源的其他支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-2815">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="6543a-2816">已新增新 'ApplicationInsights' 類型，以支援指定工作區的取得特定和取得所有 ApplicationInsights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="6543a-2816">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="6543a-2817">已新增 New-AzOperationalInsightsApplicationInsightsDataSource Cmdlet 用來建立資料來源，透過指定的 Application-Insights 資源參數：訂用帳戶識別碼、resourceGroupName 和名稱。</span><span class="sxs-lookup"><span data-stu-id="6543a-2817">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2818">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2818">Az.Resources</span></span>
* <span data-ttu-id="6543a-2819">修正 https://github.com/Azure/azure-powershell/issues/8166 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2819">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6543a-2820">修正 https://github.com/Azure/azure-powershell/issues/8235 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2820">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="6543a-2821">修正 https://github.com/Azure/azure-powershell/issues/6219 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2821">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="6543a-2822">修正防止重複建立 KeyCredentials 的錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-2822">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2823">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2823">Az.Sql</span></span>
* <span data-ttu-id="6543a-2824">新增 SQL DB 超大規模層支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2824">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="6543a-2825">已修正以下錯誤：由於在還原要求中設定非必要屬性造成還原失敗</span><span class="sxs-lookup"><span data-stu-id="6543a-2825">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2826">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2826">Az.Websites</span></span>
* <span data-ttu-id="6543a-2827">Get-AzWebAppSlotMetrics 中的正確範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2827">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="6543a-2828">1.3.0 - 2019 年 2 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2828">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2829">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2829">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2830">更新至最新版本的 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6543a-2830">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-2831">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2831">Az.AnalysisServices</span></span>
<span data-ttu-id="6543a-2832">Az.AnalysisServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="6543a-2832">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2833">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2833">Az.Compute</span></span>
* <span data-ttu-id="6543a-2834">AEM 延伸模組：新增對 UltraSSD 和 P60、P70 和 P80 磁碟的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2834">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="6543a-2835">更新 AzVMBootDiagnostics 的說明描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2835">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="6543a-2836">更新 Update-AzImage 的說明描述和範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2836">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2837">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2837">Az.RecoveryServices</span></span>
<span data-ttu-id="6543a-2838">Az.RecoveryServices 模組的正式運作。</span><span class="sxs-lookup"><span data-stu-id="6543a-2838">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2839">Az.Resources</span></span>
* <span data-ttu-id="6543a-2840">修正資源群組標記</span><span class="sxs-lookup"><span data-stu-id="6543a-2840">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="6543a-2841">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="6543a-2841">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="6543a-2842">修正 `Get-AzureRmRoleAssignment`不遵守 -ErrorAction 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2842">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="6543a-2843">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="6543a-2843">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2844">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2844">Az.Sql</span></span>
* <span data-ttu-id="6543a-2845">新增 Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6543a-2845">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="6543a-2846">修正執行 SQL Cmdlet 時無法登入 Azure 帳戶會導致 nullref 例外狀況的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2846">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="6543a-2847">已修正 Get AzSqlCapability 中的 Null 參考例外狀況</span><span class="sxs-lookup"><span data-stu-id="6543a-2847">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="6543a-2848">1.2.1 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2848">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2849">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2849">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2850">包含正確驗證版本的發行</span><span class="sxs-lookup"><span data-stu-id="6543a-2850">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="6543a-2851">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2851">Az.AnalysisServices</span></span>
* <span data-ttu-id="6543a-2852">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="6543a-2852">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-2853">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2853">Az.RecoveryServices</span></span>
* <span data-ttu-id="6543a-2854">包含更新驗證相依性的版本</span><span class="sxs-lookup"><span data-stu-id="6543a-2854">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="6543a-2855">1.2.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2855">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2856">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2857">僅新增 Windows PowerShell 5.1 互動式和使用者名稱/密碼驗證</span><span class="sxs-lookup"><span data-stu-id="6543a-2857">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="6543a-2858">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2858">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6543a-2859">在 PS Core 中新增 Uninstall-AzureRm 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-2859">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="6543a-2860">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="6543a-2860">Az.Aks</span></span>
* <span data-ttu-id="6543a-2861">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2861">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="6543a-2862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-2862">Az.Automation</span></span>
* <span data-ttu-id="6543a-2863">已新增 Python 2 Runbook 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2863">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="6543a-2864">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2864">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="6543a-2865">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="6543a-2865">Az.Cdn</span></span>
* <span data-ttu-id="6543a-2866">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2866">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2867">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2867">Az.Compute</span></span>
* <span data-ttu-id="6543a-2868">新增 Invoke-AzVMReimage Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2868">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="6543a-2869">將 TempDisk 參數新增至 Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6543a-2869">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="6543a-2870">修正 New-AzVM 的警告訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-2870">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="6543a-2871">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6543a-2871">Az.ContainerRegistry</span></span>
* <span data-ttu-id="6543a-2872">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2872">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="6543a-2873">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="6543a-2873">Az.DataFactory</span></span>
* <span data-ttu-id="6543a-2874">已將 ADF .Net SDK 版本更新為 3.0.0</span><span class="sxs-lookup"><span data-stu-id="6543a-2874">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2875">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2875">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2876">修正使用 MSI 時 ADLS 端點的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2876">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="6543a-2877">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="6543a-2877">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="6543a-2878">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2878">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-2879">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2879">Az.IotHub</span></span>
* <span data-ttu-id="6543a-2880">將編碼格式新增至 Add-IotHubRoutingEndpoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-2880">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="6543a-2881">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2881">Az.KeyVault</span></span>
* <span data-ttu-id="6543a-2882">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2882">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-2883">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2883">Az.Network</span></span>
* <span data-ttu-id="6543a-2884">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2884">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2885">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2885">Az.Resources</span></span>
* <span data-ttu-id="6543a-2886">修正 「New-AzADAppCredential」和「New-AzADSpCredential」參考文件中不正確的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-2886">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="6543a-2887">修正「-TemplateFile」參數路徑並未在執行資源群組部署 Cmdlet 前解析的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2887">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="6543a-2888">Az.Resources：正確的 New-AzureRmPolicyDefinition -Mode 預設值文件</span><span class="sxs-lookup"><span data-stu-id="6543a-2888">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="6543a-2889">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/7522 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2889">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="6543a-2890">Az.Resources：修正 https://github.com/Azure/azure-powershell/issues/5747 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2890">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="6543a-2891">修正「PSResourceGroupDeployment」物件格式化的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2891">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="6543a-2892">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="6543a-2892">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-2893">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-2893">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-2894">將憑證新增到 VMSS 模型但擲回例外狀況時復原，以修正錯誤： https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="6543a-2894">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="6543a-2895">修正某些錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-2895">Fix some error messages.</span></span>
* <span data-ttu-id="6543a-2896">修正使用預設 ARM 範本為並未移轉至 Az 的 New-AzServiceFabriCluster 建立叢集的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2896">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="6543a-2897">檢查延伸模組中的叢集識別碼，修正只將叢集/應用程式憑證新增至對應至該叢集的 VM 擴展集中的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2897">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6543a-2898">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6543a-2898">Az.SignalR</span></span>
* <span data-ttu-id="6543a-2899">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2899">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2900">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2900">Az.Sql</span></span>
* <span data-ttu-id="6543a-2901">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2901">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6543a-2902">更新了 LicenseType 參數的描述並新增了可能的值</span><span class="sxs-lookup"><span data-stu-id="6543a-2902">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="6543a-2903">修正當更新受控執行個體身分識別僅為已更新屬性時無法運作的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2903">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="6543a-2904">支援在受控執行個體上的自訂定序</span><span class="sxs-lookup"><span data-stu-id="6543a-2904">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2905">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2905">Az.Storage</span></span>
* <span data-ttu-id="6543a-2906">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2906">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6543a-2907">在進階儲存體帳戶上取得/設定傳統記錄/計量時提供詳細錯誤訊息，因為進階儲存體帳戶不支援傳統記錄/計量。</span><span class="sxs-lookup"><span data-stu-id="6543a-2907">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="6543a-2908">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="6543a-2908">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="6543a-2909">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6543a-2909">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="6543a-2910">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6543a-2910">Az.TrafficManager</span></span>
* <span data-ttu-id="6543a-2911">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2911">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2912">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2912">Az.Websites</span></span>
* <span data-ttu-id="6543a-2913">更新不正確的線上說明 URL</span><span class="sxs-lookup"><span data-stu-id="6543a-2913">Update incorrect online help URLs</span></span>
* <span data-ttu-id="6543a-2914">修正「New-AzWebAppSSLBinding」，以便在應用程式於 ASE 上託管時將憑證上傳到正確的資源群組及位置。</span><span class="sxs-lookup"><span data-stu-id="6543a-2914">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="6543a-2915">修正「New-AzWebAppSSLBinding」以便在將 SSL 憑證繫結至應用程式時不要覆寫標記</span><span class="sxs-lookup"><span data-stu-id="6543a-2915">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="6543a-2916">1.1.0 - 2019 年 1 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2916">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="6543a-2917">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2917">Az.Accounts</span></span>
* <span data-ttu-id="6543a-2918">將 'Local' 範圍新增至 Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="6543a-2918">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-2919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-2919">Az.Compute</span></span>
* <span data-ttu-id="6543a-2920">在 Restart/Start/Stop/Remove/Set-AzVM 和 Save-AzVMImage 的識別碼參數集中，名稱現在為選用項目</span><span class="sxs-lookup"><span data-stu-id="6543a-2920">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="6543a-2921">已更新說明檔案中的識別碼描述</span><span class="sxs-lookup"><span data-stu-id="6543a-2921">Updated the description of ID in help files</span></span>
* <span data-ttu-id="6543a-2922">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2922">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2923">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2923">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-2924">將資料平面的 SDK 版本更新為 1.1.14，以修正 SDK 問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-2924">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="6543a-2925">針對 getfilestatus 和 liststatus 修正 acesstime 和 modificationtime 的負值處理、修正非同步取消權杖</span><span class="sxs-lookup"><span data-stu-id="6543a-2925">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="6543a-2926">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="6543a-2926">Az.EventGrid</span></span>
* <span data-ttu-id="6543a-2927">已更新為使用 2019-01-01 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6543a-2927">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="6543a-2928">更新下列 Cmdlet 來支援 2019-01-01 API 版本中的新案例</span><span class="sxs-lookup"><span data-stu-id="6543a-2928">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="6543a-2929">New-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6543a-2929">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6543a-2930">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="6543a-2930">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6543a-2931">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="6543a-2931">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6543a-2932">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="6543a-2932">Dead letter endpoint.</span></span>
    - <span data-ttu-id="6543a-2933">Update-AzureRmEventGridSubscription:新增選擇性參數來指定：</span><span class="sxs-lookup"><span data-stu-id="6543a-2933">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="6543a-2934">事件存留時間、</span><span class="sxs-lookup"><span data-stu-id="6543a-2934">Event Time-To-Live,</span></span>
        - <span data-ttu-id="6543a-2935">嘗試傳遞事件的次數上限、</span><span class="sxs-lookup"><span data-stu-id="6543a-2935">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="6543a-2936">無效信件端點。</span><span class="sxs-lookup"><span data-stu-id="6543a-2936">Dead letter endpoint.</span></span>
* <span data-ttu-id="6543a-2937">針對 New-AzureRmEventGridSubscription 和 Update-AzureRmEventGridSubscription Cmdlet 中的 EndpointType 選項新增列舉值 (namely、storageQueue 和 hybridConnection)。</span><span class="sxs-lookup"><span data-stu-id="6543a-2937">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="6543a-2938">如果預期需要使用者手動建立或更新事件訂閱，則顯示警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-2938">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="6543a-2939">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="6543a-2939">Az.IotHub</span></span>
* <span data-ttu-id="6543a-2940">已更新至最新版本的 IotHub SDK</span><span class="sxs-lookup"><span data-stu-id="6543a-2940">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="6543a-2941">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="6543a-2941">Az.LogicApp</span></span>
* <span data-ttu-id="6543a-2942">Get-AzLogicApp 會列出所有項目，無須指定名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2942">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-2943">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-2943">Az.Resources</span></span>
* <span data-ttu-id="6543a-2944">修正為 'Get-AzResource' 提供 '-ODataQuery' 和 '-ResourceId' 參數時的參數集問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2944">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="6543a-2945">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="6543a-2945">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="6543a-2946">修正 New/Set-AzPolicyDefinition 中的 -Custom 參數處理</span><span class="sxs-lookup"><span data-stu-id="6543a-2946">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6543a-2947">修正 New-AzDeployment 文件中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-2947">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="6543a-2948">使 '-MailNickname' 參數成為 'New-AzADUser' 的必要項目</span><span class="sxs-lookup"><span data-stu-id="6543a-2948">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="6543a-2949">如需詳細資訊，請參閱這裡： https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="6543a-2949">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="6543a-2950">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="6543a-2950">Az.SignalR</span></span>
* <span data-ttu-id="6543a-2951">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2951">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-2952">Az.Sql</span></span>
* <span data-ttu-id="6543a-2953">將儲存體管理用戶端相依性轉換為一般的 SDK 實作。</span><span class="sxs-lookup"><span data-stu-id="6543a-2953">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="6543a-2954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-2954">Az.Storage</span></span>
* <span data-ttu-id="6543a-2955">使用 Sas 權杖、OAuth 或匿名來建立儲存體內容的 StorageAccountName 時，將其設定為實際的儲存體帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-2955">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="6543a-2956">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6543a-2956">New-AzStorageContext</span></span>
* <span data-ttu-id="6543a-2957">使用 '-FullUri' 參數建立 Blob 快照集物件的 Sas 權杖、將傳回的 Uri 修正為快照集 Uri</span><span class="sxs-lookup"><span data-stu-id="6543a-2957">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="6543a-2958">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="6543a-2958">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-2959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-2959">Az.Websites</span></span>
* <span data-ttu-id="6543a-2960">修正 'Get-AzDeletedWebApp' 中的日期剖析錯誤</span><span class="sxs-lookup"><span data-stu-id="6543a-2960">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="6543a-2961">修正 Az.Accounts 模組的回溯相容性問題</span><span class="sxs-lookup"><span data-stu-id="6543a-2961">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="6543a-2962">1.0.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6543a-2962">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="6543a-2963">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-2963">General</span></span>

- <span data-ttu-id="6543a-2964">Az 模組正式運作</span><span class="sxs-lookup"><span data-stu-id="6543a-2964">General Availability of Az Module</span></span>
- <span data-ttu-id="6543a-2965">每個模組的線上說明</span><span class="sxs-lookup"><span data-stu-id="6543a-2965">Online help for each module</span></span>
- <span data-ttu-id="6543a-2966">如需詳細資訊和藍圖，請參閱 [Az 公告頁面](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="6543a-2966">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="6543a-2967">如需從 AzureRM 遷移的相關資訊，請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2967">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="6543a-2968">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-2968">Az.Accounts</span></span>
- <span data-ttu-id="6543a-2969">已從 Az.Profile 變更</span><span class="sxs-lookup"><span data-stu-id="6543a-2969">Changed from Az.Profile</span></span>
- <span data-ttu-id="6543a-2970">設定檔和內容類型有固定的資料表格式</span><span class="sxs-lookup"><span data-stu-id="6543a-2970">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6543a-2971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-2971">Az.ApiManagement</span></span>
- <span data-ttu-id="6543a-2972">#7002 的修正</span><span class="sxs-lookup"><span data-stu-id="6543a-2972">Fixes for #7002</span></span>
- <span data-ttu-id="6543a-2973">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2973">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="6543a-2974">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6543a-2974">Az.Batch</span></span>
- <span data-ttu-id="6543a-2975">已新增功能，可透過 `PSComputeNode` 上新的 `NodeAgentInformation` 屬性，查看集區中每個 VM 上所執行的 Azure Batch 節點代理程式是哪個版本。</span><span class="sxs-lookup"><span data-stu-id="6543a-2975">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="6543a-2976">`PSDataDisk` 的 `Caching` 預設值現在為 `ReadWrite` 而非 `None`。</span><span class="sxs-lookup"><span data-stu-id="6543a-2976">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="6543a-2977">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2977">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="6543a-2978">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="6543a-2978">Az.Billing</span></span>
- <span data-ttu-id="6543a-2979">結合 Billing、Consumption 和 UsageAggregates Cmdlet，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2979">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="6543a-2980">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="6543a-2980">Az.CognitivServices</span></span>
- <span data-ttu-id="6543a-2981">針對 New-AzureRmCognitiveServicesAccount 作業上可用的 SkuName 和 Typem 新增完成器</span><span class="sxs-lookup"><span data-stu-id="6543a-2981">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="6543a-2982">已從 Get-AzCognitiveServicesAccountSkus 移除 GetSkusWithAccountParamSetName 參數集</span><span class="sxs-lookup"><span data-stu-id="6543a-2982">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6543a-2983">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-2983">Az.ContainerInstance</span></span>
- <span data-ttu-id="6543a-2984">已新增 ManagedIdentity 支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2984">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="6543a-2985">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="6543a-2985">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="6543a-2986">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2986">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6543a-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-2987">Az.DataLakeStore</span></span>
- <span data-ttu-id="6543a-2988">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2988">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="6543a-2989">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6543a-2989">Az.Monitor</span></span>
- <span data-ttu-id="6543a-2990">Az.Insights 已重新命名為 Az.Monitor，並有次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-2990">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="6543a-2991">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6543a-2991">Az.KeyVault</span></span>
- <span data-ttu-id="6543a-2992">已從輸出類型中移除淘汰的 'PurgeDisabled' 屬性</span><span class="sxs-lookup"><span data-stu-id="6543a-2992">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="6543a-2993">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="6543a-2993">Az.MachineLearning</span></span>
- <span data-ttu-id="6543a-2994">已納入來自 Az.MachineLearningCompute 模組的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-2994">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="6543a-2995">Az.Media</span><span class="sxs-lookup"><span data-stu-id="6543a-2995">Az.Media</span></span>
- <span data-ttu-id="6543a-2996">從 New-AzMediaService 移除淘汰的 -Tags 別名</span><span class="sxs-lookup"><span data-stu-id="6543a-2996">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6543a-2997">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-2997">Az.Network</span></span>
<span data-ttu-id="6543a-2998">已新增在應用程式閘道中設定 RewriteRuleSets 的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-2998">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="6543a-2999">已新增新的 Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6543a-2999">New cmdlets added:</span></span>
        - <span data-ttu-id="6543a-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3000">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3001">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3002">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3003">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3004">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3005">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6543a-3005">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="6543a-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3006">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="6543a-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="6543a-3007">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="6543a-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6543a-3008">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="6543a-3009">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6543a-3009">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="6543a-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6543a-3010">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6543a-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="6543a-3011">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="6543a-3012">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-3012">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="6543a-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-3013">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="6543a-3014">New-AzureRmApplicationGatewayUrlPathMapConfig 已使用身分識別對應用程式閘道新增 KeyVault 支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-3014">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="6543a-3015">已使用選擇性參數 -KeyVaultSecretId, -KeyVaultSecret 更新了 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3015">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="6543a-3016">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6543a-3016">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6543a-3017">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6543a-3017">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="6543a-3018">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="6543a-3018">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="6543a-3019">已使用選擇性參數 -UserAssignedIdentity 更新了 New-AzApplicationGateway Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3019">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="6543a-3020">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3020">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="6543a-3021">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-3021">Az.OperationalInsights</span></span>
- <span data-ttu-id="6543a-3022">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3022">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="6543a-3023">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6543a-3023">Az.Profile</span></span>
- <span data-ttu-id="6543a-3024">模組名稱已變更為 Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="6543a-3024">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-3025">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-3025">Az.RecoveryServices</span></span>
- <span data-ttu-id="6543a-3026">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3026">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="6543a-3027">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3027">Az.Resources</span></span>
- <span data-ttu-id="6543a-3028">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3028">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6543a-3029">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-3029">Az.ServiceFabric</span></span>
- <span data-ttu-id="6543a-3030">支援依通用名稱和指紋來指定憑證</span><span class="sxs-lookup"><span data-stu-id="6543a-3030">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="6543a-3031">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3031">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="6543a-3032">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="6543a-3032">Az.SIgnalR</span></span>
- <span data-ttu-id="6543a-3033">SIgnalR 的 PowerShell Cmdlet 正式運作</span><span class="sxs-lookup"><span data-stu-id="6543a-3033">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="6543a-3034">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-3034">Az.Sql</span></span>
- <span data-ttu-id="6543a-3035">已對威脅偵測的 Cmdlet 新增 Data_Exfiltration 和 Unsafe_Action 偵測類型</span><span class="sxs-lookup"><span data-stu-id="6543a-3035">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="6543a-3036">已更新 SQL 稽核 Cmdlet 的文件範例</span><span class="sxs-lookup"><span data-stu-id="6543a-3036">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="6543a-3037">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3037">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="6543a-3038">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-3038">Az.Storage</span></span>
- <span data-ttu-id="6543a-3039">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3039">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6543a-3040">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-3040">Az.Websites</span></span>
- <span data-ttu-id="6543a-3041">次要重大變更，詳情請參閱[移轉指南](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="6543a-3041">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="6543a-3042">0.7.0 - 2018 年 12 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3042">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="6543a-3043">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-3043">General</span></span>

* <span data-ttu-id="6543a-3044">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="6543a-3044">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="6543a-3045">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-3045">Az.Compute</span></span>

* <span data-ttu-id="6543a-3046">針對 `New-AzVm(ss)` Cmdlet 簡單參數集內的 UltraSSD 和資源庫映像新增支援。</span><span class="sxs-lookup"><span data-stu-id="6543a-3046">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="6543a-3047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-3047">Az.DataLakeStore</span></span>

* <span data-ttu-id="6543a-3048">修正 adls 帳戶網域的尾端斜線</span><span class="sxs-lookup"><span data-stu-id="6543a-3048">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="6543a-3049">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6543a-3049">Az.FrontDoor</span></span>

* <span data-ttu-id="6543a-3050">已修正一些中斷的連結</span><span class="sxs-lookup"><span data-stu-id="6543a-3050">Fixed some broken links</span></span>
    - <span data-ttu-id="6543a-3051">在 New-AzureRmFrontDoor 和 Set-AzureRmFrontDoor 文章中，已修正 New-AzureRmFrontDoorHealthProbeSettingObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="6543a-3051">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="6543a-3052">在 New-AzureRmFrontDoorManagedRuleObject 文章中，已修正 New-AzureRmFrontDoorRuleGroupOverrideObject Cmdlet 文章的連結。</span><span class="sxs-lookup"><span data-stu-id="6543a-3052">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="6543a-3053">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="6543a-3053">Az.RecoveryServices</span></span>

* <span data-ttu-id="6543a-3054">已針對 Azure 檔案共用的還原作業新增用戶端驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-3054">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="6543a-3055">已將 storageAccountName 和 storageAccountResourceGroupName 設為 afs 還原作業的選擇性項目。</span><span class="sxs-lookup"><span data-stu-id="6543a-3055">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="6543a-3056">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3056">Az.Resources</span></span>

* <span data-ttu-id="6543a-3057">修正 https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="6543a-3057">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="6543a-3058">將 Get-AzureRmRoleAssignment 更新為使用訂用帳戶範圍 (如果有在要求傳統管理員時提供的話)。</span><span class="sxs-lookup"><span data-stu-id="6543a-3058">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="6543a-3059">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-3059">Az.Sql</span></span>

* <span data-ttu-id="6543a-3060">即將推出的「AzureRM 對 Az 轉換」有些微變更</span><span class="sxs-lookup"><span data-stu-id="6543a-3060">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="6543a-3061">已修正搭配使用 Get-AzureRmSqlDatabaseVulnerabilityAssessment 和 DotNet core 時所會發生的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3061">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="6543a-3062">已修改 SQL 稽核 Cmdlet 相關說明訊息的文件。</span><span class="sxs-lookup"><span data-stu-id="6543a-3062">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="6543a-3063">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-3063">Az.Storage</span></span>

* <span data-ttu-id="6543a-3064">對 New-AzureRmStorageAccount 新增 -EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="6543a-3064">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="6543a-3065">已修正下列問題：如果沒有輸入 -DestContext，複製檔案 Cmdlet 無法重複使用目的地中的來源內容</span><span class="sxs-lookup"><span data-stu-id="6543a-3065">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="6543a-3066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6543a-3066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6543a-3067">支援靜態網站設定</span><span class="sxs-lookup"><span data-stu-id="6543a-3067">Support Static Website configuration</span></span>
    - <span data-ttu-id="6543a-3068">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6543a-3068">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="6543a-3069">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6543a-3069">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="6543a-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-3070">Az.Websites</span></span>

* <span data-ttu-id="6543a-3071">Set-AzureRmWebApp 和 Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6543a-3071">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="6543a-3072">已新增新的參數 (-AzureStoragePath)，指定要將 Azure 儲存體路徑掛接至 Windows 和 Linux 容器應用程式中。</span><span class="sxs-lookup"><span data-stu-id="6543a-3072">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="6543a-3073">使用新 Cmdlet New-AzureRmWebAppAzureStoragePath 的輸出作為參數來設定 Azure 儲存體路徑。</span><span class="sxs-lookup"><span data-stu-id="6543a-3073">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="6543a-3074">0.6.1 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3074">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="6543a-3075">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6543a-3075">Az.ApiManagement</span></span>
* <span data-ttu-id="6543a-3076">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-3076">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="6543a-3077">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="6543a-3077">Az.Automation</span></span>
* <span data-ttu-id="6543a-3078">以 Swagger 為基礎的 Azure 自動化 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3078">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="6543a-3079">已新增更新管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3079">Added Update Management cmdlets</span></span>
* <span data-ttu-id="6543a-3080">已新增原始檔控制 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3080">Added Source Control cmdlets</span></span>
* <span data-ttu-id="6543a-3081">已新增 Remove-AzureRmAutomationHybridWorkerGroup Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3081">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="6543a-3082">已修正 DSC 註冊節點命令</span><span class="sxs-lookup"><span data-stu-id="6543a-3082">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="6543a-3083">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-3083">Az.Compute</span></span>
* <span data-ttu-id="6543a-3084">已修正 SystemAssigned 身分識別的身份識別問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3084">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="6543a-3085">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-3085">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="6543a-3086">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-3086">Az.ContainerInstance</span></span>
* <span data-ttu-id="6543a-3087">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-3087">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="6543a-3088">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="6543a-3088">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="6543a-3089">更新市集 Cmdlet 的範例描述</span><span class="sxs-lookup"><span data-stu-id="6543a-3089">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="6543a-3090">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-3090">Az.Network</span></span>
* <span data-ttu-id="6543a-3091">已新增 Cmdlet：New-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayCustomError、Get-AzureRmApplicationGatewayCustomError、Set-AzureRmApplicationGatewayCustomError、Remove-AzureRmApplicationGatewayCustomError、Add-AzureRmApplicationGatewayHttpListenerCustomError、Get-AzureRmApplicationGatewayHttpListenerCustomError、Set-AzureRmApplicationGatewayHttpListenerCustomError、Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="6543a-3091">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="6543a-3092">已將 ICMP 加回支援的 AzureFirewall 網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="6543a-3092">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="6543a-3093">更新 Test-AzureRmNetworkWatcherConnectivity Cmdlet，在目的地識別碼、位址和連接埠上新增驗證。</span><span class="sxs-lookup"><span data-stu-id="6543a-3093">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="6543a-3094">修正 VirtualNetwork 對應中的記憶體使用量問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3094">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="6543a-3095">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="6543a-3095">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="6543a-3096">提供修正程式以修改受保護的檔案共用原則。</span><span class="sxs-lookup"><span data-stu-id="6543a-3096">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="6543a-3097">已將原則時區轉換為大寫。</span><span class="sxs-lookup"><span data-stu-id="6543a-3097">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="6543a-3098">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="6543a-3098">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="6543a-3099">已修正 New-AzureRmRecoveryServicesAsrProtectableItem 中的範例</span><span class="sxs-lookup"><span data-stu-id="6543a-3099">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="6543a-3100">針對類型對應問題更新相依性</span><span class="sxs-lookup"><span data-stu-id="6543a-3100">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="6543a-3101">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="6543a-3101">Az.Relay</span></span>
* <span data-ttu-id="6543a-3102">已將選擇性參數 -KeyValue 新增至 New-AzureRmRelayKey Cmdlet，這樣會要求使用者提供 KeyValue。</span><span class="sxs-lookup"><span data-stu-id="6543a-3102">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="6543a-3103">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3103">Az.Resources</span></span>
* <span data-ttu-id="6543a-3104">更新 `New-AzureRmPolicyAssignment` 和 `Set-AzureRmPolicyAssignment` 中資源身分識別相關參數的說明文件</span><span class="sxs-lookup"><span data-stu-id="6543a-3104">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="6543a-3105">新增使用 -Metadata 的 New-AzureRmPolicyDefinition 範例</span><span class="sxs-lookup"><span data-stu-id="6543a-3105">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="6543a-3106">修正：允許在 NetStandard: #7678 #7703 的標籤索引鍵中保留大小寫</span><span class="sxs-lookup"><span data-stu-id="6543a-3106">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="6543a-3107">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-3107">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-3108">針對即將推出的重大變更新增取代資訊</span><span class="sxs-lookup"><span data-stu-id="6543a-3108">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="6543a-3109">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-3109">Az.Sql</span></span>
* <span data-ttu-id="6543a-3110">已在 Azure SQL Database 受控執行個體和 Azure SQL 受控資料庫上新增 CRUD 作業的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3110">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="6543a-3111">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-3111">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6543a-3112">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-3112">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6543a-3113">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-3113">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6543a-3114">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="6543a-3114">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="6543a-3115">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6543a-3115">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6543a-3116">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6543a-3116">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6543a-3117">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6543a-3117">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="6543a-3118">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="6543a-3118">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="6543a-3119">已在伺服器或資料庫上啟用擴充的稽核原則管理。</span><span class="sxs-lookup"><span data-stu-id="6543a-3119">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="6543a-3120">已新增參數 (PredicateExpression) 以啟用稽核記錄的篩選。</span><span class="sxs-lookup"><span data-stu-id="6543a-3120">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="6543a-3121">已將 Cmdlet 修改為使用 SQL 用戶端，而不是傳統用戶端。</span><span class="sxs-lookup"><span data-stu-id="6543a-3121">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="6543a-3122">Set-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="6543a-3122">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6543a-3123">Get-AzureRmSqlServerAuditing。</span><span class="sxs-lookup"><span data-stu-id="6543a-3123">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="6543a-3124">Set-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="6543a-3124">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="6543a-3125">Get-AzureRmSqlDatabaseAuditing。</span><span class="sxs-lookup"><span data-stu-id="6543a-3125">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="6543a-3126">已修正使用 Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings 和儲存體帳戶名稱參數集的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3126">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="6543a-3127">0.5.0 - 2018 年 11 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3127">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="6543a-3128">一般</span><span class="sxs-lookup"><span data-stu-id="6543a-3128">General</span></span>
* <span data-ttu-id="6543a-3129">已在許多核心 Cmdlet 新增資源完成器 - 這些 Cmdlet 可讓您在以互動方式叫用 Cmdlet 時，使用 TAB 鍵瀏覽現有資源名稱</span><span class="sxs-lookup"><span data-stu-id="6543a-3129">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="6543a-3130">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6543a-3130">Az.Profile</span></span>
* <span data-ttu-id="6543a-3131">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6543a-3131">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="6543a-3132">將 Cmdlet Connect-AzAccount 中的參數 TenantId 重新命名為 Tenant 並新增 TenantId 的別名</span><span class="sxs-lookup"><span data-stu-id="6543a-3132">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="6543a-3133">更新 Connect-AzAccount 的 TenantId 說明</span><span class="sxs-lookup"><span data-stu-id="6543a-3133">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="6543a-3134">修正提供租用戶網域時登入失敗的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="6543a-3134">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="6543a-3135">修正租用戶中無訂用帳戶之帳戶內容衝突的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3135">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="6543a-3136">修正使用 MSI 時 DataLake 端點的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3136">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="6543a-3137">修正若未連線，'Disconnect-AzAccount' 會擲出錯誤的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3137">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-3138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-3138">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-3139">新增 Get-AzCognitiveServicesAccountSkus 作業。</span><span class="sxs-lookup"><span data-stu-id="6543a-3139">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-3140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-3140">Az.Compute</span></span>
* <span data-ttu-id="6543a-3141">新增 Add-AzVmssVMDataDisk 和 Remove-AzVmssVMDataDisk Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3141">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="6543a-3142">Get-AzVMImage 顯示 AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="6543a-3142">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="6543a-3143">已修正 SetAzVMChefExtension -BootstrapOptions 和 -JsonAttribute 選項值並未以 json 格式設定的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-3143">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-3144">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-3144">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-3145">將 DataLake 套件更新為 1.1.10。</span><span class="sxs-lookup"><span data-stu-id="6543a-3145">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="6543a-3146">將預設並行新增至多執行作業。</span><span class="sxs-lookup"><span data-stu-id="6543a-3146">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="6543a-3147">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="6543a-3147">Az.Insights</span></span>
* <span data-ttu-id="6543a-3148">已修正問題 #7267 (自動調整區域)</span><span class="sxs-lookup"><span data-stu-id="6543a-3148">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="6543a-3149">建立新自動調整規則時未適當設定列舉的參數 (一律會設為預設值) 的問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-3149">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="6543a-3150">已修正問題 #7513 [Insights] Set-AzDiagnosticSetting 在建立設定時需要明確的類別規格</span><span class="sxs-lookup"><span data-stu-id="6543a-3150">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="6543a-3151">目前 Cmdlet 在建立期間不需要明確的類別指示也能啟用，例如 Cmdlet 會如說明所述之方式運作</span><span class="sxs-lookup"><span data-stu-id="6543a-3151">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-3152">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-3152">Az.Network</span></span>
* <span data-ttu-id="6543a-3153">已將 PeeringType 變更為下列 Cmdlet 的必要參數：-</span><span class="sxs-lookup"><span data-stu-id="6543a-3153">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="6543a-3154">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-3154">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="6543a-3155">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6543a-3155">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="6543a-3156">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6543a-3156">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="6543a-3157">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="6543a-3157">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="6543a-3158">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="6543a-3158">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="6543a-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6543a-3159">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="6543a-3160">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="6543a-3160">Az.PolicyInsights</span></span>
* <span data-ttu-id="6543a-3161">已新增原則修復 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3161">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-3162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3162">Az.Resources</span></span>
* <span data-ttu-id="6543a-3163">修正 https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="6543a-3163">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="6543a-3164">允許使用 'Get-AzResource' 的 '-ResourceId' 參數列出資源</span><span class="sxs-lookup"><span data-stu-id="6543a-3164">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="6543a-3165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="6543a-3165">Az.ServiceBus</span></span>
* <span data-ttu-id="6543a-3166">已將 MigrationState 唯讀屬性新增至 PSServiceBusMigrationConfigurationAttributes，以便協助了解移轉狀態。</span><span class="sxs-lookup"><span data-stu-id="6543a-3166">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="6543a-3167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6543a-3167">Az.ServiceFabric</span></span>
* <span data-ttu-id="6543a-3168">修正將憑證新增至 Linux Vmss。</span><span class="sxs-lookup"><span data-stu-id="6543a-3168">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="6543a-3169">修正 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="6543a-3169">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="6543a-3170">使用新憑證中正確的指紋 (Azure/service-fabric-issues#932)。</span><span class="sxs-lookup"><span data-stu-id="6543a-3170">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="6543a-3171">正確顯示例外狀況 (Azure/service-fabric-issues#1054)。</span><span class="sxs-lookup"><span data-stu-id="6543a-3171">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="6543a-3172">修正 'Update-AzServiceFabricDurability' 以在啟動 Vmss CreateOrUpdate operation 之前更新叢集組態。</span><span class="sxs-lookup"><span data-stu-id="6543a-3172">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="6543a-3173">0.4.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3173">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="6543a-3174">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="6543a-3174">Az.Profile</span></span>
* <span data-ttu-id="6543a-3175">修正 CloudShell 中 Get-AzSubscription 的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3175">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="6543a-3176">更新通用程式碼，以使用最新版 ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="6543a-3176">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-3177">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-3177">Az.Compute</span></span>
* <span data-ttu-id="6543a-3178">已將新的大小新增至虛擬機器大小允許清單，當使用 'New-AzVm' 的簡單參數集合時，將會開啟加速的網路</span><span class="sxs-lookup"><span data-stu-id="6543a-3178">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="6543a-3179">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-3179">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="6543a-3180">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="6543a-3180">Az.DataLakeStore</span></span>
* <span data-ttu-id="6543a-3181">新增虛擬網路規則的支援</span><span class="sxs-lookup"><span data-stu-id="6543a-3181">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="6543a-3182">Get-AzDataLakeStoreVirtualNetworkRule：取得或列出 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6543a-3182">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="6543a-3183">Add-AzDataLakeStoreVirtualNetworkRule：將虛擬網路規則新增至指定的 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="6543a-3183">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6543a-3184">Set-AzDataLakeStoreVirtualNetworkRule：修改指定 Data Lake Store 帳戶中的特定虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6543a-3184">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="6543a-3185">Remove-AzDataLakeStoreVirtualNetworkRule：刪除 Azure Data Lake Store 的虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="6543a-3185">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-3186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-3186">Az.Network</span></span>
* <span data-ttu-id="6543a-3187">更新 Cmdlet Test-AzNetworkWatcherConnectivity，將通訊協定值傳遞至後端。</span><span class="sxs-lookup"><span data-stu-id="6543a-3187">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="6543a-3188">已將 ResourceName 引數完成器新增至所有 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6543a-3188">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-3189">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3189">Az.Resources</span></span>
* <span data-ttu-id="6543a-3190">修正當 Get-AzRoleDefinition 藉由在案例中加上有意義的例外狀況，而擲回無法辨識的例外狀況 (當預設的設定檔中沒有訂用帳戶，且未指定範圍) 問題。</span><span class="sxs-lookup"><span data-stu-id="6543a-3190">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="6543a-3191">也將預設參數集合設定為 'RoleDefinitionNameParameterSet'。</span><span class="sxs-lookup"><span data-stu-id="6543a-3191">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="6543a-3192">0.3.0 - 2018 年 10 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3192">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="6543a-3193">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="6543a-3193">Azure.Storage</span></span>
* <span data-ttu-id="6543a-3194">修正當目的地有中繼資料問題時，複製 Blob/檔案不會一併複製中繼資料的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3194">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="6543a-3195">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="6543a-3195">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="6543a-3196">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="6543a-3196">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="6543a-3197">支援取得特定位置的儲存體資源使用量，並針對取得全域儲存體資源使用量已過時的情況新增警告訊息。</span><span class="sxs-lookup"><span data-stu-id="6543a-3197">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="6543a-3198">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="6543a-3198">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="6543a-3199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="6543a-3199">Az.CognitiveServices</span></span>
* <span data-ttu-id="6543a-3200">在沒有現有帳戶的情況下支援 Get-AzCognitiveServicesAccountSkus。</span><span class="sxs-lookup"><span data-stu-id="6543a-3200">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="6543a-3201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6543a-3201">Az.Compute</span></span>
* <span data-ttu-id="6543a-3202">修正 Get-AzVM -ResourceGroupName <rg> 以在必要時傳回超過 50 個結果</span><span class="sxs-lookup"><span data-stu-id="6543a-3202">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="6543a-3203">已將 'SimpleParameterSet' 的範例新增到 New-AzVmss Cmdlet 說明中。</span><span class="sxs-lookup"><span data-stu-id="6543a-3203">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="6543a-3204">已修正 Azure 磁碟加密進度訊息中的錯字</span><span class="sxs-lookup"><span data-stu-id="6543a-3204">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="6543a-3205">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6543a-3205">Az.DataFactoryV2</span></span>
* <span data-ttu-id="6543a-3206">已將 ADF .Net SDK 版本更新為 2.3.0。</span><span class="sxs-lookup"><span data-stu-id="6543a-3206">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="6543a-3207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6543a-3207">Az.Network</span></span>
* <span data-ttu-id="6543a-3208">已新增 NetworkProfile 功能。</span><span class="sxs-lookup"><span data-stu-id="6543a-3208">Added NetworkProfile functionality.</span></span> <span data-ttu-id="6543a-3209">已新增新的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3209">new cmdlets added</span></span>
    - <span data-ttu-id="6543a-3210">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6543a-3210">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="6543a-3211">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6543a-3211">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="6543a-3212">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6543a-3212">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="6543a-3213">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="6543a-3213">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="6543a-3214">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-3214">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="6543a-3215">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="6543a-3215">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="6543a-3216">已在子網路模型中新增服務關聯連結</span><span class="sxs-lookup"><span data-stu-id="6543a-3216">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="6543a-3217">已新增 New-AzVirtualNetworkTap、Get-AzVirtualNetworkTap、Set-AzVirtualNetworkTap、Remove-AzVirtualNetworkTap Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3217">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="6543a-3218">已新增 Set-AzNEtworkInterfaceTapConfig、Get-AzNEtworkInterfaceTapConfig 和 Remove-AzNEtworkInterfaceTapConfig Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6543a-3218">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="6543a-3219">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="6543a-3219">Az.RedisCache</span></span>
* <span data-ttu-id="6543a-3220">日後允許任何字串做為 Size 參數。</span><span class="sxs-lookup"><span data-stu-id="6543a-3220">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="6543a-3221">在 P5 PSArgumentCompleter 快顯視窗中新增 P5</span><span class="sxs-lookup"><span data-stu-id="6543a-3221">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="6543a-3222">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6543a-3222">Az.Resources</span></span>
* <span data-ttu-id="6543a-3223">將遺漏的 -Mode 參數新增至 Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6543a-3223">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="6543a-3224">修正 Get-AzProviderOperation Commandlet 錯誤 (bug)，以進行包含使用者的 Origin 作業</span><span class="sxs-lookup"><span data-stu-id="6543a-3224">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="6543a-3225">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="6543a-3225">Az.Sql</span></span>
* <span data-ttu-id="6543a-3226">已修正部分備份 Cmdlet 無法辨識目前 Azure 訂用帳戶的問題</span><span class="sxs-lookup"><span data-stu-id="6543a-3226">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="6543a-3227">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="6543a-3227">Az.Websites</span></span>
* <span data-ttu-id="6543a-3228">新 Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - 取得容器連續部署 Webhook URL</span><span class="sxs-lookup"><span data-stu-id="6543a-3228">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="6543a-3229">新 Cmdlet New-AzWebAppContainerPSSession 與 Enter-WebAppContainerPSSession  - 在 Windows 容器應用程式中初始 PowerShell 遠端工作階段</span><span class="sxs-lookup"><span data-stu-id="6543a-3229">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="6543a-3230">0.2.0 - 2018 年 9 月</span><span class="sxs-lookup"><span data-stu-id="6543a-3230">0.2.0 - September 2018</span></span>
 <span data-ttu-id="6543a-3231">初始版本</span><span class="sxs-lookup"><span data-stu-id="6543a-3231">Initial Release</span></span>
