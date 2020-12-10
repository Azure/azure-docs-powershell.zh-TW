---
title: Az 5.0.0 的移轉指南
description: 本移轉指南包含在 Az 5.0.0 版發行中對 Azure PowerShell 進行中斷性變更的清單。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856145"
---
# <a name="migration-guide-for-az-500"></a>Az 5.0.0 的移轉指南

本文件說明 Az 4.0.0 與 5.0.0 版之間的變更。

- [Az 5.0.0 的移轉指南](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- 不再支援參數 `NodeOsType`，而且找不到原始參數名稱的別名，其一律會是 `Linux`。
- 不再支援參數 `ServicePrincipalIdAndSecret` 的別名 `ClientIdAndSecret`。
- `NodeVmSetType` 的預設值會從 `AvailabilitySet` 變更為 `VirtualMachineScaleSets`。
- `NetworkPlugin` 的預設值會從 `none` 變更為 `azure`。

#### <a name="before"></a>之前

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>在

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

不再支援參數 `ServicePrincipalIdAndSecret` 的別名 `ClientIdAndSecret`。

#### <a name="before"></a>之前

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>在

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

不再支援參數 `StorageAccountName` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>在

已淘汰 `Classic` 並已移除 `StorageAccountName`，因為其只適用於傳統容器登錄。

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

已從 `Get-AzFunctionApp` 的所有參數集 (一個參數集除外) 中移除 `IncludeSlot` 切換參數。 若已指定 `-IncludeSlot`，此 Cmdlet 現在支援在結果中擷取部署位置。
這項功能在先前的 Cmdlet 版本中已中斷。 不過，現在已修正此問題。

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- 已修正 `New-AzFunctionApp` 中的 `-DisableApplicationInsights`，若已指定此選項，就不會建立 Application Insights 專案。
- 已移除建立 PowerShell 6.2 函式應用程式的支援，因為 PowerShell 6.2 是 EOL。 客戶目前的指引是改為建立 PowerShell 7.0 函式應用程式。
- 若未指定 `RuntimeVersion` 參數，Windows 上 Functions 第 3 版中 PowerShell 函式應用程式的預設執行階段版本已從 6.2 變更為 7.0。
- 若未指定 `RuntimeVersion` 參數，Windows 和 Linux 上 Functions 第 3 版中 Node 函式應用程式的預設執行階段版本已從 10 變更為 12。 不過，使用者仍可藉由指定 `-Runtime Node` 和 `-RuntimeVersion 10`來建立 Node 10 函式應用程式。 若未指定 `RuntimeVersion` 參數，Linux 上 Functions 第 3 版中 Python 函式應用程式的預設執行階段版本已從 3.7 變更為 3.8。 不過，使用者仍可藉由指定 `-Runtime Python` 和 `-RuntimeVersion 3.7`來建立 Python 3.7 函式應用程式。

#### <a name="before"></a>之前

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

#### <a name="after"></a>在

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

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

不再支援參數 `DisableSoftDelete` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>在

在 Az. KeyVault 3.0.0 中，已淘汰更新虛刪除設定的功能。 閱讀更多： https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

不再支援參數 `EnableSoftDelete`、`SoftDeleteRetentionInDays`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>在

在 Az. KeyVault 3.0.0 中，已淘汰更新虛刪除設定的功能。 閱讀更多： https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

已移除 `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` 類型的 `SecretValueText` 屬性。 `SecretValueText` 屬性已取代為 `SecretValue`。

#### <a name="before"></a>之前

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>在

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

不再支援參數 `ResourceId` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>在

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

不再支援參數 `RegistrationDefinitionName`、`RegistrationDefinitionResourceId`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>在

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

不再支援參數 `Id`、`ResourceId`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>在

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

不再支援參數 `Id`、`ResourceId`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>在

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

不再支援參數 `ApiVersion` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>在

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azdeployment"></a>Get-AzDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="new-azdeployment"></a>New-AzDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="remove-azdeployment"></a>Remove-AzDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="stop-azdeployment"></a>Stop-AzDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="test-azdeployment"></a>Test-AzDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

與 `Get-AzManagementGroupDeployment` 相同。

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

與 `Get-AzManagementGroupDeployment` 相同。

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

不再支援參數 `IsAzureADOnlyAuthentication` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>在

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

不再支援參數 `FromBackup`、`FromRestorePoint`、`BackupResourceGroupName`、`BackupWorkspaceName`、`BackupSqlPoolName`、`BackupSqlPoolObject`、`BackupResourceId`、`SourceResourceGroupName`、`SourceWorkspaceName`、`SourceSqlPoolName`、`SourceSqlPoolObject`、`SourceResourceId`、`RestorePoint`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>在

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

不再支援參數 `Suspend`、`Resume`，而且找不到原始參數名稱的別名。

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

不再支援參數 `PrivateLinkResourceType` ，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>在

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

與 `Approve-AzPrivateEndpointConnection` 相同。

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

與 `Approve-AzPrivateEndpointConnection` 相同。

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

與 `Approve-AzPrivateEndpointConnection` 相同。

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

與 `Approve-AzPrivateEndpointConnection` 相同。

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

不再支援參數 `FilterType`、`FilterItem`，而且找不到原始參數名稱的別名。

#### <a name="before"></a>之前

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>After

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
