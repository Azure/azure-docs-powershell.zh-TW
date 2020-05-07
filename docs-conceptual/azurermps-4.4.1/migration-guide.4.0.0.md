---
title: Microsoft Azure PowerShell 4.0.0 的重大變更
description: 本移轉指南包含在第 4 版發行中對 Azure PowerShell 進行重大變更的清單。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 2f61e41b701dfc263df18064f6ac2cc4c6e4021e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "67863544"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a>Microsoft Azure PowerShell 4.0.0 的重大變更

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。 每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。 如需深入了解內容，請參閱與每次變更相關聯的提取要求。

## <a name="table-of-contents"></a>目錄

- [Compute Cmdlet 的重大變更](#breaking-changes-to-compute-cmdlets)
- [EventHub Cmdlet 的重大變更](#breaking-changes-to-eventhub-cmdlets)
- [Insights Cmdlet 的重大變更](#breaking-changes-to-insights-cmdlets)
- [Network Cmdlet 的重大變更](#breaking-changes-to-network-cmdlets)
- [ServiceBus Cmdlet 的重大變更](#breaking-changes-to-servicebus-cmdlets)
- [Sql Cmdlet 的重大變更](#breaking-changes-to-sql-cmdlets)
- [Storage Cmdlet 的重大變更](#breaking-changes-to-storage-cmdlets)
- [Profile Cmdlet 的重大變更](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a>Compute Cmdlet 的重大變更

受到此版本影響的輸出類型如下：

### <a name="psvirtualmachine"></a>PSVirtualMachine
- `DataDiskNames` 物件的最上層屬性 `NetworkInterfaceIDs` 和 `PSVirtualMachine` 已從輸出類型中移除。 這些屬性已一律可在 `StorageProfile` 物件的 `NetworkProfile` 和 `PSVirtualMachine` 屬性中使用，並需要繼續透過存取方式取得。
- 這項變更會影響下列 Cmdlet：
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub Cmdlet 的重大變更

受到此版本影響的 Cmdlet 如下：

### <a name="get-azurermeventhubnamespace"></a>Get-AzureRmEventHubNamespace
- `ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除

### <a name="new-azurermeventhubnamespace"></a>New-AzureRmEventHubNamespace
- `ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除

## <a name="breaking-changes-to-insights-cmdlets"></a>Insights Cmdlet 的重大變更

受到此版本影響的 Cmdlet 如下：
    
### <a name="get-azurermusage"></a>Get-AzureRmUsage
- 此 Cmdlet 已受到取代。

### <a name="remove-azurermalertrule"></a>Remove-AzureRmAlertRule
- 此 Cmdlet 的輸出已從具有單一物件的清單變更為單一物件，此物件包含 requestId 和狀態碼。
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a>Add-AzureRmLogAlertRule
- 此 Cmdlet 已受到取代。
    
### <a name="get-azurermalertrule"></a>Get-AzureRmAlertRule
- 此 Cmdlet 輸出 (物件清單) 的每個元素會經過壓平合併，也就是並非以 `{ Id, Location, Name, Tags, Properties }` 結構傳回物件，而是以 `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}` 結構傳回物件，該結構是 Azure Resource 的所有屬性和最上層 AlertRuleResource 的所有屬性。
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a>Get-AzureRmAutoscaleSetting
- `AutoscaleSettingResourceName` 欄位會受到取代，因為它一律與 `Name` 欄位有相同的值。

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a>Remove-AzureRmLogProfile
- 此 Cmdlet 的輸出將會從 `Boolean` 變更為物件，其中包含 `RequestId` 和 `StatusCode`

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a>Add-AzureRmLogProfile
- 此 Cmdlet 的輸出會變更為包含 requestId、狀態碼和已更新或新建立資源的物件
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a>Set-AzureRmDiagnosticSettings
- 此命令將重新命名為 `Update-AzureRmDiagnosticSettings`

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a>Network Cmdlet 的重大變更

受到此版本影響的 Cmdlet 如下：

### <a name="new-azurermvirtualnetworkgatewayconnection"></a>New-AzureRmVirtualNetworkGatewayConnection
- `EnableBgp` 參數已變更為採用 `boolean`，而不是採用 `string`

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus Cmdlet 的重大變更

受到此版本影響的 Cmdlet 如下：

### <a name="get-azurermservicebusnamespace"></a>Get-AzureRmServiceBusNamespace
- `ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除

### <a name="new-azurermservicebusnamespace"></a>New-AzureRmServiceBusNamespace

- `ResourceGroupName` 屬性已從輸出類型 `NamespaceAttributes` 中移除

## <a name="breaking-changes-to-sql-cmdlets"></a>Sql Cmdlet 的重大變更

受到此版本影響的 Cmdlet 如下：

### <a name="new-azurermsqldatabasefailovergroup"></a>New-AzureRmSqlDatabaseFailoverGroup
- `Tag` 參數已移除
- `GracePeriodWithDataLossHour` 參數已重新命名為 `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a>Set-AzureRmSqlDatabaseFailoverGroup
- `Tag` 參數已移除
- `GracePeriodWithDataLossHour` 參數已重新命名為 `GracePeriodWithDataLossHours`

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a>Add-AzureRmSqlDatabaseToFailoverGroup
- `Tag` 參數已移除

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a>Remove-AzureRmSqlDatabaseFromFailoverGroup
- `Tag` 參數已移除

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a>Remove-AzureRmSqlDatabaseFailoverGroup
- `PartnerResourceGroupName` 參數已移除
- `PartnerServerName` 參數已移除

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a>Set-AzureRmSqlDatabaseThreatDetectionPolicy
- `Usage_Anomaly` 值已不再是 `ExcludedDetectionType` 參數的有效值

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a>Set-AzureRmSqlServerThreatDetectionPolicy
- `Usage_Anomaly` 值已不再是 `ExcludedDetectionType` 參數的有效值

## <a name="breaking-changes-to-storage-cmdlets"></a>Storage Cmdlet 的重大變更

受到此版本影響的輸出類型參數如下：

### <a name="azurestorageblobicloudblobserviceclient"></a>AzureStorageBlob.ICloudBlob.ServiceClient
- 下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到):
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 這項變更會影響下列 Cmdlet：
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a>AzureStorageContainer.CloudBlobContainer.ServiceClient
- 下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- 這項變更會影響下列 Cmdlet：
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a>AzureStorageQueue.CloudQueue.ServiceClient
- 下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- 這項變更會影響下列 Cmdlet：
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a>AzureStorageTable.CloudTable.ServiceClient
- 下列屬性已從此類型中移除 (_注意_：這些屬性還是可以在 `DefaultRequestOptions` 屬性中找到)：
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- 這項變更會影響下列 Cmdlet：
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a>Profile Cmdlet 的重大變更

下列 Cmdlet 與 Cmdlet 輸出類型已在此版本中變更。

### <a name="add-azurermaccount-breaking-changes"></a>Add-AzureRmAccount 重大變更

- ```EnvironmentName``` 已移除，並以 ```Environment``` 加以取代，```Environment``` 現在會採用字串，而不是採用 ```AzureEnvironment``` 物件

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a>Select-AzureRmProfile 已重新命名為 Import-AzureRmContext

```Select-AzureRmProfile``` 已重新命名為 ```Import-AzureRmContext```

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a>Save-AzureRmProfile 已重新命名為 Save-AzureRmContext

```Save-AzureRmProfile``` 已重新命名為 ```Save-AzureRmContext```

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a>PSAzureContext 類型輸出的重大變更

- ```TokenCache``` 屬性已變更為實作 ```IAzureTokenCache``` 的類型，而不是實作 ```byte[]``` 的類型

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a>PSAzureAccount 類型輸出的重大變更

- ```AccountType``` 屬性已變更為 ```Type```

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a>PSAzureSubscription 類型輸出的重大變更
- ```SubscriptionId``` 屬性已變更為 ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- ```SubscriptionName``` 屬性已變更為 ```Name```

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a>PSAzureTenant 類型輸出的重大變更

- ```TenantId``` 屬性已變更為 ```Id```

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- ```Domain``` 屬性已變更為 ```Directory```

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
