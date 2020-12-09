---
title: Az 4.1.0 的移轉指南
description: 本移轉指南包含在 Az 4.1.0 版發行中對 Azure PowerShell 進行重大變更的清單。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: fe4a2a7c2f1b171b530eef41ac072b2029be1026
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715161"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="afb17-103">Az 4.1.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="afb17-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="afb17-104">本文件說明 Az 3.0.0 與 4.1.0 版之間的變更。</span><span class="sxs-lookup"><span data-stu-id="afb17-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="afb17-105">Az 4.1.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="afb17-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="afb17-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="afb17-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="afb17-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="afb17-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="afb17-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="afb17-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="afb17-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="afb17-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="afb17-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="afb17-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="afb17-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="afb17-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="afb17-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="afb17-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="afb17-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="afb17-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="afb17-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="afb17-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="afb17-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="afb17-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="afb17-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="afb17-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="afb17-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="afb17-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="afb17-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="afb17-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="afb17-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="afb17-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="afb17-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="afb17-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="afb17-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="afb17-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="afb17-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="afb17-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="afb17-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="afb17-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="afb17-124">`Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` 類型的 `Type` 屬性類型已從 `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` 變更為 `System.String`。</span><span class="sxs-lookup"><span data-stu-id="afb17-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="afb17-125">Cmdlet `New-AzApiManagement` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-126">已移除 Cmdlet `New-AzApiManagement` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="afb17-127">Cmdlet `Set-AzApiManagement` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-128">已移除 Cmdlet `Set-AzApiManagement` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="afb17-129">Cmdlet `Get-AzApiManagementProperty` 已由 `Get-AzApiManagementNamedValue` 取代。</span><span class="sxs-lookup"><span data-stu-id="afb17-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="afb17-130">Cmdlet `New-AzApiManagementProperty` 已由 `New-AzApiManagementNamedValue` 取代。</span><span class="sxs-lookup"><span data-stu-id="afb17-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="afb17-131">Cmdlet `Remove-AzApiManagementProperty` 已由 `Remove-AzApiManagementNamedValue` 取代。</span><span class="sxs-lookup"><span data-stu-id="afb17-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="afb17-132">Cmdlet `Set-AzApiManagementProperty` 已由 `Set-AzApiManagementNamedValue` 取代。</span><span class="sxs-lookup"><span data-stu-id="afb17-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="afb17-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="afb17-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="afb17-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="afb17-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="afb17-135">已移除 `Microsoft.Azure.Commands.Batch.Models.PSApplication` 類型的 `ApplicationPackages` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="afb17-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="afb17-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="afb17-137">已移除 `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` 類型的 `PublicIPs` 屬性</span><span class="sxs-lookup"><span data-stu-id="afb17-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="afb17-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="afb17-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="afb17-139">`Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` 類型的 `StorageUrlExpiry` 屬性類型已從 `System.DateTime` 變更為 `System.DateTime?`。</span><span class="sxs-lookup"><span data-stu-id="afb17-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="afb17-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="afb17-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="afb17-141">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="afb17-142">Cmdlet `Get-AzVMImage` 已不再支援參數 `FilterExpression`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-143">已移除 Cmdlet `Get-AzVMImage` 的參數集 `ListVMImage`。</span><span class="sxs-lookup"><span data-stu-id="afb17-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="afb17-144">Cmdlet `New-AzVMConfig` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-145">已移除 Cmdlet `New-AzVMConfig` 的參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="afb17-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="afb17-146">Cmdlet `Update-AzVM` 已不再支援參數 `AssignIdentity`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-147">已移除 Cmdlet `Update-AzVM` 的參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="afb17-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="afb17-148">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="afb17-149">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-150">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="afb17-151">After</span><span class="sxs-lookup"><span data-stu-id="afb17-151">After</span></span>

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

- <span data-ttu-id="afb17-152">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="afb17-153">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-154">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="afb17-155">After</span><span class="sxs-lookup"><span data-stu-id="afb17-155">After</span></span>

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

- <span data-ttu-id="afb17-156">`VirtualMachines`、`VirtualMachineScaleSets` 和 `AvailabilitySets` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="afb17-157">已移除 `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` 類型的 `VirtualMachinesColocationStatus`、`VirtualMachineScaleSetsColocationStatus` 和 `AvailabilitySetsColocationStatus` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-158">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="afb17-159">After</span><span class="sxs-lookup"><span data-stu-id="afb17-159">After</span></span>

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

<span data-ttu-id="afb17-160">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="afb17-161">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="afb17-162">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="afb17-163">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="afb17-164">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="afb17-165">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="afb17-166">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="afb17-167">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="afb17-168">不再支援參數 `AutomaticRepairMaxInstanceRepairsPercent` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-169">不再支援參數 `AssignIdentity` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-170">已移除參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="afb17-171">已移除參數集 `ExplicitIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="afb17-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="afb17-172">已移除參數集 `AssignIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="afb17-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="afb17-173">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="afb17-174">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="afb17-175">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="afb17-176">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="afb17-177">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="afb17-178">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="afb17-179">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="afb17-180">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="afb17-181">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="afb17-182">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="afb17-183">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="afb17-184">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="afb17-185">不再支援參數 `AutomaticRepairMaxInstanceRepairsPercent` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-186">已移除參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="afb17-187">已移除參數集 `ExplicitIdentityParameterSet`。</span><span class="sxs-lookup"><span data-stu-id="afb17-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="afb17-188">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="afb17-189">`Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` 類型的 `AutomaticRepairsPolicy` 屬性類型已從 `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` 變更為 `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="afb17-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="afb17-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="afb17-191">已移除 `New-AzKeyVaultCertificateOrganizationDetails` 別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="afb17-192">請使用 `New-AzKeyVaultCertificateOrganizationDetail`。</span><span class="sxs-lookup"><span data-stu-id="afb17-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-193">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="afb17-194">After</span><span class="sxs-lookup"><span data-stu-id="afb17-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="afb17-195">已移除 `New-AzKeyVaultCertificateAdministratorDetails` 別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="afb17-196">請使用 `New-AzKeyVaultCertificateAdministratorDetail`。</span><span class="sxs-lookup"><span data-stu-id="afb17-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-197">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="afb17-198">After</span><span class="sxs-lookup"><span data-stu-id="afb17-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="afb17-199">已移除 `-EnableSoftDelete` ，因為預設會啟用虛刪除。</span><span class="sxs-lookup"><span data-stu-id="afb17-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="afb17-200">如果您不需要此行為，請使用 `-DisableSoftDelete`。</span><span class="sxs-lookup"><span data-stu-id="afb17-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-201">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="afb17-202">After</span><span class="sxs-lookup"><span data-stu-id="afb17-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="afb17-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="afb17-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="afb17-204">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 類型的 `RetentionPolicy` 屬性類型已從 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` 變更為 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="afb17-205">`Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` 類型的 `RetentionPolicy` 屬性類型已從 `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` 變更為 `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`。</span><span class="sxs-lookup"><span data-stu-id="afb17-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="afb17-206">已移除 Cmdlet `New-AzMetricAlertRuleV2Criteria` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="afb17-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="afb17-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="afb17-208">`RoundTripTimeMs` 屬性的泛型型別已從 `System.Nullable1[System.Int32]` 變更為 `System.Nullable1[System.Double]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="afb17-209">`SuccessThresholdRoundTripTimeMs` 參數的泛型型別已從 `System.Nullable1[System.Int32]` 變更為 `System.Nullable1[System.Double]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="afb17-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="afb17-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="afb17-211">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="afb17-212">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="afb17-213">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="afb17-214">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="afb17-215">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="afb17-216">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="afb17-217">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="afb17-218">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="afb17-219">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="afb17-220">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="afb17-221">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="afb17-222">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="afb17-223">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="afb17-224">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="afb17-225">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="afb17-226">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="afb17-227">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="afb17-228">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` 類型的 `Metadata` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="afb17-229">SDK 不再支援 Cmdlet `Get-AzOperationalInsightsSavedSearchResult`，且已將其移除。</span><span class="sxs-lookup"><span data-stu-id="afb17-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="afb17-230">SDK 不再支援 Cmdlet `Get-AzOperationalInsightsSearchResult`，且已將其移除。</span><span class="sxs-lookup"><span data-stu-id="afb17-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="afb17-231">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="afb17-232">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="afb17-233">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="afb17-234">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="afb17-235">SDK 不再支援 Cmdlet `Get-AzOperationalInsightsLinkTarget`，且已將其移除。</span><span class="sxs-lookup"><span data-stu-id="afb17-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="afb17-236">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="afb17-237">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="afb17-238">Cmdlet `New-AzOperationalInsightsWorkspace` 已不再支援參數 `CustomerId`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="afb17-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="afb17-239">已移除 Cmdlet `New-AzOperationalInsightsWorkspace` 的參數集 `__AllParameterSets`。</span><span class="sxs-lookup"><span data-stu-id="afb17-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="afb17-240">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="afb17-241">已移除 `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` 類型的 `PortalUrl` 屬性。</span><span class="sxs-lookup"><span data-stu-id="afb17-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="afb17-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="afb17-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="afb17-243">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="afb17-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="afb17-244">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="afb17-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="afb17-245">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="afb17-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="afb17-246">已移除參數 `TenantLevel`。</span><span class="sxs-lookup"><span data-stu-id="afb17-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="afb17-247">`Aliases` 屬性的泛型型別已從 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` 變更為 `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`。</span><span class="sxs-lookup"><span data-stu-id="afb17-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="afb17-248">Cmdlet `New-AzPolicyAssignment` 不再支援參數 `PolicyDefinition` 的類型 `System.Management.Automation.PSObject`。</span><span class="sxs-lookup"><span data-stu-id="afb17-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="afb17-249">Cmdlet `New-AzPolicyAssignment` 不再支援參數 `PolicySetDefinition` 的類型 `System.Management.Automation.PSObject`。</span><span class="sxs-lookup"><span data-stu-id="afb17-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="afb17-250">`Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` 類型的 `Status` 屬性類型已從 `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` 變更為 `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`。</span><span class="sxs-lookup"><span data-stu-id="afb17-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="afb17-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="afb17-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="afb17-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="afb17-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="afb17-253">已將 NetWorkRule DefaultAction 值從允許 = 1，拒絕 = 0 變更為允許 = 0，拒絕 = 1。</span><span class="sxs-lookup"><span data-stu-id="afb17-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="afb17-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="afb17-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="afb17-255">輸出物件 AzureStorageTable.CloudTable.ServiceClient 已移除 2 個屬性：ConnectionPolicy、ConsistencyLevel。</span><span class="sxs-lookup"><span data-stu-id="afb17-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="afb17-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="afb17-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="afb17-257">將輸出類型從 CloudFile 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 "CloudFile"</span><span class="sxs-lookup"><span data-stu-id="afb17-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-258">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="afb17-259">After</span><span class="sxs-lookup"><span data-stu-id="afb17-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="afb17-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="afb17-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="afb17-261">將輸出類型從 CloudFileDirectory 變更為 AzureStorageFileDirectory，原始輸出將成為新輸出的子屬性 "CloudFileDirectory"</span><span class="sxs-lookup"><span data-stu-id="afb17-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-262">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="afb17-263">After</span><span class="sxs-lookup"><span data-stu-id="afb17-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="afb17-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="afb17-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="afb17-265">將輸出類型從 FileShareProperties 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 "CloudFileShare"</span><span class="sxs-lookup"><span data-stu-id="afb17-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-266">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="afb17-267">After</span><span class="sxs-lookup"><span data-stu-id="afb17-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="afb17-268">將輸出類型從 FileShareProperties 變更為 AzureStorageFile，原始輸出將成為新輸出的子屬性 ""CloudFileShare.Properties""</span><span class="sxs-lookup"><span data-stu-id="afb17-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-269">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="afb17-270">After</span><span class="sxs-lookup"><span data-stu-id="afb17-270">After</span></span>

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

<span data-ttu-id="afb17-271">移除具有上層目錄物件和 -Path 的子檔案目錄時，無法再從類型 (字串) 相符的管道中輸入 -Path。</span><span class="sxs-lookup"><span data-stu-id="afb17-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="afb17-272">之前</span><span class="sxs-lookup"><span data-stu-id="afb17-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="afb17-273">After</span><span class="sxs-lookup"><span data-stu-id="afb17-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```