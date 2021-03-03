---
title: Az 5.0.0 的移轉指南
description: 本移轉指南包含在 Az 5.0.0 版發行中對 Azure PowerShell 進行中斷性變更的清單。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684929"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="8440e-103">Az 5.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="8440e-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="8440e-104">本文件說明 Az 4.0.0 與 5.0.0 版之間的變更。</span><span class="sxs-lookup"><span data-stu-id="8440e-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="8440e-105">Az 5.0.0 的移轉指南</span><span class="sxs-lookup"><span data-stu-id="8440e-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="8440e-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8440e-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="8440e-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8440e-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="8440e-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8440e-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="8440e-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8440e-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="8440e-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8440e-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="8440e-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8440e-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="8440e-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8440e-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="8440e-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8440e-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="8440e-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="8440e-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="8440e-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="8440e-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8440e-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="8440e-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8440e-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="8440e-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8440e-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="8440e-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8440e-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="8440e-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8440e-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="8440e-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8440e-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="8440e-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="8440e-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="8440e-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="8440e-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="8440e-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="8440e-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="8440e-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="8440e-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="8440e-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="8440e-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="8440e-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="8440e-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="8440e-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="8440e-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="8440e-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="8440e-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="8440e-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="8440e-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="8440e-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="8440e-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="8440e-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="8440e-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="8440e-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="8440e-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="8440e-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="8440e-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="8440e-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="8440e-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="8440e-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="8440e-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="8440e-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="8440e-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="8440e-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="8440e-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="8440e-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8440e-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="8440e-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8440e-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="8440e-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="8440e-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="8440e-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8440e-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="8440e-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8440e-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="8440e-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8440e-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="8440e-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="8440e-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="8440e-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="8440e-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="8440e-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="8440e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8440e-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="8440e-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="8440e-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="8440e-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8440e-169">New-AzAksCluster</span></span>

- <span data-ttu-id="8440e-170">不再支援參數 `NodeOsType`，而且找不到原始參數名稱的別名，其一律會是 `Linux`。</span><span class="sxs-lookup"><span data-stu-id="8440e-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="8440e-171">不再支援參數 `ServicePrincipalIdAndSecret` 的別名 `ClientIdAndSecret`。</span><span class="sxs-lookup"><span data-stu-id="8440e-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="8440e-172">`NodeVmSetType` 的預設值會從 `AvailabilitySet` 變更為 `VirtualMachineScaleSets`。</span><span class="sxs-lookup"><span data-stu-id="8440e-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="8440e-173">`NetworkPlugin` 的預設值會從 `none` 變更為 `azure`。</span><span class="sxs-lookup"><span data-stu-id="8440e-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-174">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-175">在</span><span class="sxs-lookup"><span data-stu-id="8440e-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="8440e-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8440e-176">Set-AzAksCluster</span></span>

<span data-ttu-id="8440e-177">不再支援參數 `ServicePrincipalIdAndSecret` 的別名 `ClientIdAndSecret`。</span><span class="sxs-lookup"><span data-stu-id="8440e-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-178">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-179">在</span><span class="sxs-lookup"><span data-stu-id="8440e-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="8440e-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8440e-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="8440e-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8440e-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="8440e-182">不再支援參數 `StorageAccountName` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-183">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="8440e-184">在</span><span class="sxs-lookup"><span data-stu-id="8440e-184">After</span></span>

<span data-ttu-id="8440e-185">已淘汰 `Classic` 並已移除 `StorageAccountName`，因為其只適用於傳統容器登錄。</span><span class="sxs-lookup"><span data-stu-id="8440e-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="8440e-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="8440e-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="8440e-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8440e-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="8440e-188">已從 `Get-AzFunctionApp` 的所有參數集 (一個參數集除外) 中移除 `IncludeSlot` 切換參數。</span><span class="sxs-lookup"><span data-stu-id="8440e-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="8440e-189">若已指定 `-IncludeSlot`，此 Cmdlet 現在支援在結果中擷取部署位置。</span><span class="sxs-lookup"><span data-stu-id="8440e-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="8440e-190">這項功能在先前的 Cmdlet 版本中已中斷。</span><span class="sxs-lookup"><span data-stu-id="8440e-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="8440e-191">不過，現在已修正此問題。</span><span class="sxs-lookup"><span data-stu-id="8440e-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="8440e-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8440e-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="8440e-193">已修正 `New-AzFunctionApp` 中的 `-DisableApplicationInsights`，若已指定此選項，就不會建立 Application Insights 專案。</span><span class="sxs-lookup"><span data-stu-id="8440e-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="8440e-194">已移除建立 PowerShell 6.2 函式應用程式的支援，因為 PowerShell 6.2 是 EOL。</span><span class="sxs-lookup"><span data-stu-id="8440e-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="8440e-195">客戶目前的指引是改為建立 PowerShell 7.0 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="8440e-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="8440e-196">若未指定 `RuntimeVersion` 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。</span><span class="sxs-lookup"><span data-stu-id="8440e-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="8440e-197">若未指定 `RuntimeVersion` 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。</span><span class="sxs-lookup"><span data-stu-id="8440e-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="8440e-198">不過，使用者仍可藉由指定 `-Runtime Node` 和 `-RuntimeVersion 10`來建立 Node 10 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="8440e-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="8440e-199">若未指定 `RuntimeVersion` 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。</span><span class="sxs-lookup"><span data-stu-id="8440e-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="8440e-200">不過，使用者仍可藉由指定 `-Runtime Python` 和 `-RuntimeVersion 3.7`來建立 Python 3.7 函式應用程式。</span><span class="sxs-lookup"><span data-stu-id="8440e-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-201">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="8440e-202">在</span><span class="sxs-lookup"><span data-stu-id="8440e-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="8440e-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="8440e-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-204">New-AzKeyVault</span></span>

<span data-ttu-id="8440e-205">不再支援參數 `DisableSoftDelete` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-206">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="8440e-207">在</span><span class="sxs-lookup"><span data-stu-id="8440e-207">After</span></span>

<span data-ttu-id="8440e-208">在 Az. KeyVault 3.0.0 中，已淘汰更新虛刪除設定的功能。</span><span class="sxs-lookup"><span data-stu-id="8440e-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="8440e-209">閱讀更多： https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="8440e-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="8440e-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8440e-210">Update-AzKeyVault</span></span>

<span data-ttu-id="8440e-211">不再支援參數 `EnableSoftDelete`、`SoftDeleteRetentionInDays`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-212">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="8440e-213">在</span><span class="sxs-lookup"><span data-stu-id="8440e-213">After</span></span>

<span data-ttu-id="8440e-214">在 Az. KeyVault 3.0.0 中，已淘汰更新虛刪除設定的功能。</span><span class="sxs-lookup"><span data-stu-id="8440e-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="8440e-215">閱讀更多： https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="8440e-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="8440e-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="8440e-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="8440e-217">已移除 `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` 類型的 `SecretValueText` 屬性。</span><span class="sxs-lookup"><span data-stu-id="8440e-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="8440e-218">請將套用 `-AsPlainText` 至呼叫以取得純文字秘密，或 `$secret.SecretValue` `SecureString` 在您的腳本中使用類型。</span><span class="sxs-lookup"><span data-stu-id="8440e-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-219">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="8440e-220">在</span><span class="sxs-lookup"><span data-stu-id="8440e-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="8440e-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="8440e-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="8440e-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8440e-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="8440e-223">不再支援參數 `ResourceId` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-224">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-225">在</span><span class="sxs-lookup"><span data-stu-id="8440e-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="8440e-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8440e-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="8440e-227">不再支援參數 `RegistrationDefinitionName`、`RegistrationDefinitionResourceId`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-228">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-229">在</span><span class="sxs-lookup"><span data-stu-id="8440e-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="8440e-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="8440e-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="8440e-231">不再支援參數 `Id`、`ResourceId`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-232">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-233">在</span><span class="sxs-lookup"><span data-stu-id="8440e-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="8440e-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="8440e-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="8440e-235">不再支援參數 `Id`、`ResourceId`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-236">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-237">在</span><span class="sxs-lookup"><span data-stu-id="8440e-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="8440e-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="8440e-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="8440e-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8440e-240">不再支援參數 `ApiVersion` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-241">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-242">在</span><span class="sxs-lookup"><span data-stu-id="8440e-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="8440e-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="8440e-244">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="8440e-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-245">Get-AzDeployment</span></span>

<span data-ttu-id="8440e-246">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="8440e-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="8440e-248">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="8440e-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="8440e-250">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="8440e-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="8440e-252">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="8440e-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="8440e-254">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="8440e-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8440e-256">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="8440e-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-257">New-AzDeployment</span></span>

<span data-ttu-id="8440e-258">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="8440e-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="8440e-260">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="8440e-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8440e-262">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="8440e-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-263">Remove-AzDeployment</span></span>

<span data-ttu-id="8440e-264">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="8440e-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="8440e-266">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="8440e-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="8440e-268">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="8440e-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="8440e-270">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="8440e-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="8440e-272">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="8440e-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8440e-274">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="8440e-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-275">Stop-AzDeployment</span></span>

<span data-ttu-id="8440e-276">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="8440e-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="8440e-278">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="8440e-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="8440e-280">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="8440e-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-281">Test-AzDeployment</span></span>

<span data-ttu-id="8440e-282">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="8440e-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="8440e-284">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="8440e-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8440e-286">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="8440e-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8440e-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="8440e-288">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="8440e-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="8440e-290">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="8440e-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8440e-292">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="8440e-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8440e-294">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="8440e-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8440e-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="8440e-296">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="8440e-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8440e-298">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="8440e-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8440e-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="8440e-300">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="8440e-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="8440e-302">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="8440e-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="8440e-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="8440e-304">與 `Get-AzManagementGroupDeployment` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="8440e-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="8440e-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="8440e-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8440e-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="8440e-307">不再支援參數 `IsAzureADOnlyAuthentication` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-308">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="8440e-309">在</span><span class="sxs-lookup"><span data-stu-id="8440e-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="8440e-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="8440e-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="8440e-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8440e-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="8440e-312">不再支援參數 `FromBackup`、`FromRestorePoint`、`BackupResourceGroupName`、`BackupWorkspaceName`、`BackupSqlPoolName`、`BackupSqlPoolObject`、`BackupResourceId`、`SourceResourceGroupName`、`SourceWorkspaceName`、`SourceSqlPoolName`、`SourceSqlPoolObject`、`SourceResourceId`、`RestorePoint`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-313">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="8440e-314">在</span><span class="sxs-lookup"><span data-stu-id="8440e-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="8440e-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="8440e-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="8440e-316">不再支援參數 `Suspend`、`Resume`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="8440e-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="8440e-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="8440e-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8440e-319">不再支援參數 `PrivateLinkResourceType` ，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-320">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="8440e-321">在</span><span class="sxs-lookup"><span data-stu-id="8440e-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="8440e-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8440e-323">與 `Approve-AzPrivateEndpointConnection` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="8440e-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8440e-325">與 `Approve-AzPrivateEndpointConnection` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="8440e-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8440e-327">與 `Approve-AzPrivateEndpointConnection` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="8440e-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8440e-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="8440e-329">與 `Approve-AzPrivateEndpointConnection` 相同。</span><span class="sxs-lookup"><span data-stu-id="8440e-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="8440e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="8440e-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="8440e-331">不再支援參數 `FilterType`、`FilterItem`，而且找不到原始參數名稱的別名。</span><span class="sxs-lookup"><span data-stu-id="8440e-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="8440e-332">之前</span><span class="sxs-lookup"><span data-stu-id="8440e-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="8440e-333">After</span><span class="sxs-lookup"><span data-stu-id="8440e-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
