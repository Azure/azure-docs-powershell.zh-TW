---
title: Microsoft Azure PowerShell 6.0.0 的重大變更
description: 本移轉指南包含在第 6 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 39d9fa6e354c3c3448053c9cdc98fdc7f55b068d
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/22/2018
ms.locfileid: "52259443"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a>Microsoft Azure PowerShell 6.0.0 的重大變更

本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。 每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。 如需深入了解內容，請參閱與每次變更相關聯的提取要求。

## <a name="table-of-contents"></a>目錄

- [一般重大變更](#general-breaking-changes)
    - [移至 5.0 所需的最低 PowerShell 版本](#minimum-powershell-version-required-bumped-to-50)
    - [依預設啟用內容自動儲存](#context-autosave-enabled-by-default)
    - [移除標記別名](#removal-of-tags-alias)
- [AzureRM.Compute Cmdlet 的重大變更](#breaking-changes-to-azurermcompute-cmdlets)
- [AzureRM.DataLakeStore Cmdlet 的重大變更](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [AzureRM.Dns Cmdlet 的重大變更](#breaking-changes-to-azurermdns-cmdlets)
- [AzureRM.Insights Cmdlet 的重大變更](#breaking-changes-to-azurerminsights-cmdlets)
- [AzureRM.KeyVault Cmdlet 的重大變更](#breaking-changes-to-azurermkeyvault-cmdlets)
- [AzureRM.Network Cmdlet 的重大變更](#breaking-changes-to-azurermnetwork-cmdlets)
- [AzureRM.RedisCache Cmdlet 的重大變更](#breaking-changes-to-azurermrediscache-cmdlets)
- [AzureRM.Resources Cmdlet 的重大變更](#breaking-changes-to-azurermresources-cmdlets)
- [AzureRM.Storage Cmdlet 的重大變更](#breaking-changes-to-azurermstorage-cmdlets)
- [移除的模組](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a>一般重大變更

### <a name="minimum-powershell-version-required-bumped-to-50"></a>移至 5.0 所需的最低 PowerShell 版本

以前，Azure PowerShell _至少需要_ PowerShell 版本 3.0，才能執行任何 Cmdlet。 日後，此需求將提升至 PowerShell 版本 5.0。 如需升級至 PowerShell 5.0 的詳細資訊，請參閱[此表格](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell)。

### <a name="context-autosave-enabled-by-default"></a>依預設啟用內容自動儲存

內容自動儲存是 Azure 登入資訊的儲存體，可以在全新和不同的 PowerShell 工作階段之間使用。 如需內容自動儲存的詳細資訊，請參閱[此文件](https://docs.microsoft.com/powershell/azure/context-persistence)。

之前，內容自動儲存會依預設停用，這表示在使用者執行 `Enable-AzureRmContextAutosave` Cmdlet 開啟內容持續性之前，系統不會儲存工作階段之間的使用者 Azure 驗證資訊。 未來，內容自動儲存將會依預設啟用，這表示若使用者_並未針對已儲存的內容設定自動儲存_，會在他們下次登入時儲存內容。 使用者可以藉由使用 `Disable-AzureRmContextAutosave` Cmdlet 來選擇退出此功能。

_注意_：先前已停用內容自動儲存或已啟用內容自動儲存的使用者，以及現有的內容將不會受到此變更影響

### <a name="removal-of-tags-alias"></a>移除標記別名

已在多個 Cmdlet 中移除 `Tag` 參數的別名 `Tags`。 以下是受此影響的模組清單 (以及對應的 Cmdlet)：

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a>AzureRM.Compute Cmdlet 的重大變更

**其他**
- 在類型 `PSDisk` 和 `PSSnapshot` 中形成巢狀的 SKU 名稱屬性，已分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

```powershell-interactive
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- 在類型 `PSVirtualMachine`、`PSVirtualMachineScaleSet` 和 `PSImage` 中形成巢狀的儲存體帳戶類型，已分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

```powershell-interactive
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

**Add-AzureRmImageDataDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Add-AzureRmVMDataDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Add-AzureRmVmssDataDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmAvailabilitySet**
- 已移除參數 `Managed` 以支持 `Sku`

```powershell-interactive
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

**New-AzureRmDiskConfig**
- 參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmDiskUpdateConfig**
- 參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmSnapshotConfig**
- 參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**New-AzureRmSnapshotUpdateConfig**
- 參數 `SkuName` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmImageOsDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVMAEMExtension**
- 已移除參數 `DisableWAD`
    -  Windows Azure 診斷預設為停用

**Set-AzureRmVMDataDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVMOSDisk**
- 參數 `StorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Set-AzureRmVmssStorageProfile**
- 參數 `ManagedDisk` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

**Update-AzureRmVmss**
- 參數 `ManagedDiskStorageAccountType` 可接受的值分別從 `StandardLRS` 和 `PremiumLRS` 變更為 `Standard_LRS` 和 `Premium_LRS`

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a>AzureRM.DataLakeStore Cmdlet 的重大變更

**Export-AzureRmDataLakeStoreItem**
- 已移除參數 `PerFileThreadCount` 和 `ConcurrentFileCount`。 未來請使用 `Concurrency` 參數

```powershell-interactive
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

**Import-AzureRmDataLakeStoreItem**
- 已移除參數 `PerFileThreadCount` 和 `ConcurrentFileCount`。 未來請使用 `Concurrency` 參數

```powershell-interactive
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

**Remove-AzureRmDataLakeStoreItem**
- 已移除參數 `Clean`

```powershell-interactive
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a>AzureRM.Dns Cmdlet 的重大變更

**New-AzureRmDnsRecordSet**
- 已移除參數 `Force`

**Remove-AzureRmDnsRecordSet**
- 已移除參數 `Force`

**Remove-AzureRmDnsZone**
- 已移除參數 `Force`

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a>AzureRM.Insights Cmdlet 的重大變更

**Add-AzureRmAutoscaleSetting**
- 已移除參數別名 `AutoscaleProfiles` 和 `Notifications`

**Add-AzureRmLogProfile**
- 已移除參數別名 `Categories` 和 `Locations`

**Add-AzureRmMetricAlertRule**
- 已移除參數別名 `Actions`

**Add-AzureRmWebtestAlertRule**
- 已移除參數別名 `Actions`

**Get-AzureRmLog**
- 已移除參數別名 `MaxRecords` 和 `MaxEvents`

**Get-AzureRmMetricDefinition**
- 已移除參數別名 `MetricNames`

**New-AzureRmAlertRuleEmail**
- 已移除參數別名 `CustomEmails` 和 `SendToServiceOwners`

**New-AzureRmAlertRuleWebhook**
- 已移除參數別名 `Properties`

**New-AzureRmAutoscaleNotification**
- 已移除參數別名 `CustomEmails`、`SendEmailToSubscriptionCoAdministrators` 和 `Webhooks`

**New-AzureRmAutoscaleProfile**
- 已移除參數別名 `Rules`、`ScheduleDays`、`ScheduleHours` 和 `ScheduleMinutes`

**New-AzureRmAutoscaleWebhook**
- 已移除參數別名 `Properties`

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a>AzureRM.KeyVault Cmdlet 的重大變更

**Add-AzureKeyVaultCertificate**
- `CertificatePolicy` 參數已變成強制參數。

**Set-AzureKeyVaultManagedStorageSasDefinition**
- 此 Cmdlet 不再接受組成存取權杖的個別參數；相反地，Cmdlet 會取代明確的存取權杖參數，例如 `Service` 或 `Permissions`，並使用泛型 `TemplateUri` 參數，對應至在其他位置定義的範例存取權杖 (假定使用的是儲存體 PowerShell Cmdlet，或是依據儲存體文件手動組成。)此 Cmdlet 會保留 `ValidityPeriod` 參數。

如需撰寫 Azure 儲存體共用存取權杖的詳細資訊，請分別參閱以下文件頁面：
- [建構服務 SAS](https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)
- [建構帳戶 SAS](https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)

```powershell-interactive
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

**Set-AzureKeyVaultCertificateIssuer**
- `IssuerProvider` 參數已變成強制參數。

**Undo-AzureKeyVaultCertificateRemoval**
- 此 Cmdlet 的輸出已從 `CertificateBundle` 變更為 `PSKeyVaultCertificate`。

**Undo-AzureRmKeyVaultRemoval**
- 已從 `InputObject` 參數集移除 `ResourceGroupName`，並改為從 `InputObject` 參數的 `ResourceId` 屬性取得。

**Set-AzureRmKeyVaultAccessPolicy**
- 已從 `PermissionsToKeys`、`PermissionsToSecrets` 和 `PermissionsToCertificates` 中移除 `all` 權限。

**一般**
- 已從已啟用 `InputObject` 管線的所有 Cmdlet 中移除 `ValueFromPipelineByPropertyName` 屬性。  受影響的 Cmdlet 為：
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- 已從所有 Cmdlet 中移除 `ConfirmImpact` 層級。  受影響的 Cmdlet 為：
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- `IKeyVaultDataServiceClient` 已更新，使得所有憑證作業會傳回 PSTypes 而不是 SDK 類型。 其中包括：
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a>AzureRM.Network Cmdlet 的重大變更


**Add-AzureRmApplicationGatewayBackendHttpSettings**
- 已移除參數 `ProbeEnabled`

**Add-AzureRmVirtualNetworkPeering**
- 已移除參數別名 `AlloowGatewayTransit`

**New-AzureRmApplicationGatewayBackendHttpSettings**
- 已移除參數 `ProbeEnabled`

**Set-AzureRmApplicationGatewayBackendHttpSettings**
- 已移除參數 `ProbeEnabled`

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a>AzureRM.RedisCache Cmdlet 的重大變更

**New-AzureRmRedisCache**
- 已移除參數 `Subnet` 和 `VirtualNetwork` 以支持 `SubnetId`
- 已移除參數 `RedisVersion`
- 已移除參數 `MaxMemoryPolicy` 以支持 `RedisConfiguration`

```powershell-interactive
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

**Set-AzureRmRedisCache**
- 已移除參數 `MaxMemoryPolicy` 以支持 `RedisConfiguration`

```powershell-interactive
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a>AzureRM.Resources Cmdlet 的重大變更

**Find-AzureRmResource**
- 已移除此 Cmdlet，並將功能移至 `Get-AzureRmResource`

```powershell-interactive
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

**Find-AzureRmResourceGroup**
- 已移除此 Cmdlet，並將功能移至 `Get-AzureRmResourceGroup`

```powershell-interactive
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

**Get-AzureRmRoleDefinition**
- 已移除參數 `AtScopeAndBelow`。

```powershell-interactive

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a>AzureRM.Storage Cmdlet 的重大變更

**New-AzureRmStorageAccount**
- 已移除參數 `EnableEncryptionService`

**Set-AzureRmStorageAccount**
- 已移除參數 `EnableEncryptionService` 和 `DisableEncryptionService`

## <a name="removed-modules"></a>移除的模組

### `AzureRM.ServerManagement`

伺服器管理工具服務已在[去年淘汰](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/)；因此，SMT 的對應模組 `AzureRM.ServerManagement`已從 `AzureRM` 移除，並將在日後停止傳送。

### `AzureRM.SiteRecovery`

已由 `AzureRM.RecoveryServices.SiteRecovery` 取代的 `AzureRM.SiteRecovery` 模組，是 `AzureRM.SiteRecovery` 模組的功能超集，並包含一組新的對等 Cmdlet。 您可以在下方找到從舊到新 Cmdlet 對應的完整清單：

| 已取代的 Cmdlet                                        | 對等的 Cmdlet                                                | 別名                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
