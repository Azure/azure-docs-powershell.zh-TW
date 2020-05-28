---
ms.openlocfilehash: 636fd0432d421f74fa74f3275abbc31ec5dc0b5c
ms.sourcegitcommit: 31f4facf815c2e25dc44e2fde0e1d2bd690bfc54
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/20/2020
ms.locfileid: "83688521"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="96111-101">Az 4.1.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="96111-101">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="96111-102">本文件說明 Az 3.0.0 與 4.1.0 版之間的變更。</span><span class="sxs-lookup"><span data-stu-id="96111-102">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="96111-103">Az 4.1.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="96111-103">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="96111-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96111-104">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="96111-105">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96111-105">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="96111-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="96111-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="96111-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="96111-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="96111-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="96111-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="96111-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96111-109">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="96111-110">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96111-110">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="96111-111">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96111-111">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="96111-112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96111-112">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="96111-113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96111-113">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="96111-114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96111-114">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="96111-115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96111-115">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="96111-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="96111-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="96111-117">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="96111-117">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="96111-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="96111-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="96111-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="96111-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="96111-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="96111-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="96111-121">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="96111-121">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="96111-122">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` 類型的 `Type` 屬性類型已從 `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` 變更為 `System.String`。</span><span class="sxs-lookup"><span data-stu-id="96111-122">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="96111-123">Cmdlet `New-AzApiManagement` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-123">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-124">已移除 Cmdlet `New-AzApiManagement` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-124">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="96111-125">Cmdlet `Set-AzApiManagement` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-125">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-126">已移除 Cmdlet `Set-AzApiManagement` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-126">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="96111-127">已移除 Cmdlet `Get-AzApiManagementProperty`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-127">The cmdlet `Get-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="96111-128">已移除 Cmdlet `New-AzApiManagementProperty`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-128">The cmdlet `New-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="96111-129">已移除 Cmdlet `Remove-AzApiManagementProperty`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-129">The cmdlet `Remove-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="96111-130">已移除 Cmdlet `Set-AzApiManagementProperty`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-130">The cmdlet `Set-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

## <a name="azbatch"></a><span data-ttu-id="96111-131">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="96111-131">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="96111-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="96111-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="96111-133">已移除 `Microsoft.Azure.Commands.Batch.Models.PSApplication` 類型的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-133">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="96111-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="96111-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="96111-135">已移除 `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` 類型的 `PublicIPs` 屬性</span><span class="sxs-lookup"><span data-stu-id="96111-135">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="96111-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="96111-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="96111-137">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` 類型的 `StorageUrlExpiry` 屬性類型已從 `System.DateTime` 變更為 `System.DateTime?`。</span><span class="sxs-lookup"><span data-stu-id="96111-137">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="96111-138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="96111-138">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="96111-139">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-139">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="96111-140">Cmdlet `Get-AzVMImage` 已不再支援參數 `FilterExpression`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-140">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-141">已移除 Cmdlet `Get-AzVMImage` 的參數集 `ListVMImage`。</span><span class="sxs-lookup"><span data-stu-id="96111-141">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="96111-142">Cmdlet `New-AzVMConfig` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-142">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-143">已移除 Cmdlet `New-AzVMConfig` 的參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="96111-143">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="96111-144">Cmdlet `Update-AzVM` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-144">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-145">已移除 Cmdlet `Update-AzVM` 的參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="96111-145">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="96111-146">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="96111-146">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="96111-147">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-147">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-148">之前</span><span class="sxs-lookup"><span data-stu-id="96111-148">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="96111-149">After</span><span class="sxs-lookup"><span data-stu-id="96111-149">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="96111-150">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="96111-150">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="96111-151">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-151">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-152">之前</span><span class="sxs-lookup"><span data-stu-id="96111-152">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="96111-153">After</span><span class="sxs-lookup"><span data-stu-id="96111-153">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="96111-154">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="96111-154">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="96111-155">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-155">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-156">之前</span><span class="sxs-lookup"><span data-stu-id="96111-156">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="96111-157">After</span><span class="sxs-lookup"><span data-stu-id="96111-157">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="96111-158">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-158">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="96111-159">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-159">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="96111-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="96111-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="96111-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="96111-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="96111-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="96111-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="96111-166">不再支援參數 `AutomaticRepairMaxInstanceRepairsPercent` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-166">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-167">不再支援參數 `AssignIdentity` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-167">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-168">已移除參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-168">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="96111-169">已移除參數集 `ExplicitIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="96111-169">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="96111-170">已移除參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="96111-170">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="96111-171">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-171">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="96111-172">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-172">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="96111-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="96111-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="96111-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="96111-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="96111-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="96111-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="96111-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="96111-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="96111-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="96111-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="96111-183">不再支援參數 `AutomaticRepairMaxInstanceRepairsPercent` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-183">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-184">已移除參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-184">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="96111-185">已移除參數集 `ExplicitIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="96111-185">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="96111-186">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-186">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="96111-187">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-187">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="96111-188">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="96111-188">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="96111-189">已移除 `New-AzKeyVaultCertificateOrganizationDetails` 別名。</span><span class="sxs-lookup"><span data-stu-id="96111-189">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="96111-190">請使用 `New-AzKeyVaultCertificateOrganizationDetail`。</span><span class="sxs-lookup"><span data-stu-id="96111-190">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-191">之前</span><span class="sxs-lookup"><span data-stu-id="96111-191">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="96111-192">After</span><span class="sxs-lookup"><span data-stu-id="96111-192">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="96111-193">已移除 `New-AzKeyVaultCertificateAdministratorDetails` 別名。</span><span class="sxs-lookup"><span data-stu-id="96111-193">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="96111-194">請使用 `New-AzKeyVaultCertificateAdministratorDetail`。</span><span class="sxs-lookup"><span data-stu-id="96111-194">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-195">之前</span><span class="sxs-lookup"><span data-stu-id="96111-195">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="96111-196">After</span><span class="sxs-lookup"><span data-stu-id="96111-196">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="96111-197">已移除 `-EnableSoftDelete` ，因為預設會啟用虛刪除。</span><span class="sxs-lookup"><span data-stu-id="96111-197">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="96111-198">如果您不需要此行為，請使用 `-DisableSoftDelete`。</span><span class="sxs-lookup"><span data-stu-id="96111-198">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-199">之前</span><span class="sxs-lookup"><span data-stu-id="96111-199">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="96111-200">After</span><span class="sxs-lookup"><span data-stu-id="96111-200">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="96111-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="96111-201">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="96111-202">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 類型的 `RetentionPolicy` 屬性類型已從 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` 變更為 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-202">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="96111-203">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 類型的 `RetentionPolicy` 屬性類型已從 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` 變更為 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`。</span><span class="sxs-lookup"><span data-stu-id="96111-203">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="96111-204">已移除 Cmdlet `New-AzMetricAlertRuleV2Criteria` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-204">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="96111-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="96111-205">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="96111-206">`RoundTripTimeMs` 屬性的泛型型別已從 `System.Nullable1[System.Int32]` 變更為 `System.Nullable1[System.Double]`。</span><span class="sxs-lookup"><span data-stu-id="96111-206">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="96111-207">`SuccessThresholdRoundTripTimeMs` 參數的泛型型別已從 `System.Nullable1[System.Int32]` 變更為 `System.Nullable1[System.Double]`。</span><span class="sxs-lookup"><span data-stu-id="96111-207">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="96111-208">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="96111-208">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="96111-209">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-209">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="96111-210">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-210">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="96111-211">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="96111-212">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="96111-213">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="96111-214">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="96111-215">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="96111-216">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="96111-217">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="96111-218">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="96111-219">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="96111-220">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="96111-221">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="96111-222">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="96111-223">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="96111-224">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="96111-225">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="96111-226">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` 類型的 `Metadata` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-226">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="96111-227">已移除 Cmdlet `Get-AzOperationalInsightsSavedSearchResult`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-227">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="96111-228">已移除 Cmdlet `Get-AzOperationalInsightsSearchResult`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-228">The cmdlet `Get-AzOperationalInsightsSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="96111-229">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-229">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="96111-230">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-230">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="96111-231">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="96111-232">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="96111-233">已移除 Cmdlet `Get-AzOperationalInsightsLinkTarget`，而且找不到原始 Cmdlet 名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-233">The cmdlet `Get-AzOperationalInsightsLinkTarget` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="96111-234">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="96111-235">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-235">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="96111-236">Cmdlet `New-AzOperationalInsightsWorkspace` 已不再支援參數 `CustomerId`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="96111-236">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="96111-237">已移除 Cmdlet `New-AzOperationalInsightsWorkspace` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="96111-237">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="96111-238">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-238">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="96111-239">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="96111-239">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="96111-240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="96111-240">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="96111-241">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="96111-241">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="96111-242">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="96111-242">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="96111-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="96111-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="96111-244">已移除參數 `TenantLevel`。</span><span class="sxs-lookup"><span data-stu-id="96111-244">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="96111-245">`Aliases` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`。</span><span class="sxs-lookup"><span data-stu-id="96111-245">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="96111-246">Cmdlet `New-AzPolicyAssignment` 不再支援參數 `PolicyDefinition` 的類型 `System.Management.Automation.PSObject`。</span><span class="sxs-lookup"><span data-stu-id="96111-246">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="96111-247">Cmdlet `New-AzPolicyAssignment` 不再支援參數 `PolicySetDefinition` 的類型 `System.Management.Automation.PSObject`。</span><span class="sxs-lookup"><span data-stu-id="96111-247">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="96111-248">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="96111-248">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="96111-249">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="96111-249">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="96111-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="96111-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="96111-251">已將 NetWorkRule DefaultAction 值從允許 = 1，拒絕 = 0 變更為允許 = 0，拒絕 = 1。</span><span class="sxs-lookup"><span data-stu-id="96111-251">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="96111-252">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="96111-252">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="96111-253">輸出物件 AzureStorageTable.CloudTable.ServiceClient 已移除 2 個屬性：ConnectionPolicy、ConsistencyLevel。</span><span class="sxs-lookup"><span data-stu-id="96111-253">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="96111-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="96111-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="96111-255">將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 "CloudFile"</span><span class="sxs-lookup"><span data-stu-id="96111-255">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="96111-256">之前</span><span class="sxs-lookup"><span data-stu-id="96111-256">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="96111-257">After</span><span class="sxs-lookup"><span data-stu-id="96111-257">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="96111-258">`Get-AzStorageFile`、`New-AzStorageDirectory`、`Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="96111-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="96111-259">將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性 "CloudFileDirectory"</span><span class="sxs-lookup"><span data-stu-id="96111-259">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="96111-260">之前</span><span class="sxs-lookup"><span data-stu-id="96111-260">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="96111-261">After</span><span class="sxs-lookup"><span data-stu-id="96111-261">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="96111-262">`Get-AzStorageShare`、`New-AzStorageShare`、`Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="96111-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="96111-263">將輸出類型從 FileShareProperties 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 "CloudFileShare"</span><span class="sxs-lookup"><span data-stu-id="96111-263">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="96111-264">之前</span><span class="sxs-lookup"><span data-stu-id="96111-264">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="96111-265">After</span><span class="sxs-lookup"><span data-stu-id="96111-265">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="96111-266">將輸出類型從 FileShareProperties 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 ""CloudFileShare.Properties""</span><span class="sxs-lookup"><span data-stu-id="96111-266">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="96111-267">之前</span><span class="sxs-lookup"><span data-stu-id="96111-267">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="96111-268">After</span><span class="sxs-lookup"><span data-stu-id="96111-268">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="96111-269">移除具有上層目錄物件和 -Path 的子檔案目錄時，無法再從類型 (字串) 相符的管道中輸入 -Path。</span><span class="sxs-lookup"><span data-stu-id="96111-269">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="96111-270">之前</span><span class="sxs-lookup"><span data-stu-id="96111-270">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="96111-271">After</span><span class="sxs-lookup"><span data-stu-id="96111-271">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
