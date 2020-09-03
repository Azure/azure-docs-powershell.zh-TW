---
title: Microsoft Azure PowerShell 5.0.0 的重大變更
description: 本移轉指南包含在第 5 版發行中對 Azure PowerShell 進行重大變更的清單。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 81f52ee8b84f60d59a7f2d53b6675129ac054fd6
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243730"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Microsoft Azure PowerShell 5.0.0 的重大變更

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

本文件為 Microsoft Azure PowerShell Cmdlet 的客戶提供重大變更通知和移轉指南。 每一節都會說明促成重大變更的原因和阻力最小的移轉路徑。 如需深入了解內容，請參閱與每次變更相關聯的提取要求。

## <a name="table-of-contents"></a>目錄

- [ApiManagement Cmdlet 的重大變更](#breaking-changes-to-apimanagement-cmdlets)
- [Batch Cmdlet 的重大變更](#breaking-changes-to-batch-cmdlets)
- [Compute Cmdlet 的重大變更](#breaking-changes-to-compute-cmdlets)
- [EventHub Cmdlet 的重大變更](#breaking-changes-to-eventhub-cmdlets)
- [Insights Cmdlet 的重大變更](#breaking-changes-to-insights-cmdlets)
- [Network Cmdlet 的重大變更](#breaking-changes-to-network-cmdlets)
- [Resources Cmdlet 的重大變更](#breaking-changes-to-resources-cmdlets)
- [ServiceBus Cmdlet 的重大變更](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>ApiManagement Cmdlet 的重大變更

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- PSCredential 將取代 "UserName" 和 "Password" 參數

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Batch Cmdlet 的重大變更

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Secure 字串將取代 `Password` 參數

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Secure 字串將取代 `Password` 參數

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Secure 字串將取代 `Password` 參數

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - 移除 `RunElevated` 參數，並以 `UserIdentity` 加以取代。

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

此動作額外影響了 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 上的 `RunElevated` 屬性。

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- `PSMultiInstanceSettings` 建構函式不再採用必要的 `numberOfInstances` 參數，而是採用必要的 `coordinationCommandLine` 參數。

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - 已將 `RunElevated` 屬性從 `PSCloudTask` 上移除。 新增 `UserIdentity` 屬性以取代 `RunElevated`。

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

此動作額外影響了 `PSCloudTask`、`PSStartTask`、`PSJobManagerTask`、`PSJobPreparationTask` 和 `PSJobReleaseTask` 上的 `RunElevated` 屬性。

### <a name="multiple-types"></a>**多種類型**

- 已將 `PSExitConditions` 上的 `SchedulingError` 屬性重新命名為 `PreProcessingError`。

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**多種類型**

- 已將 `PSJobPreparationTaskExecutionInformation`、`PSJobReleaseTaskExecutionInformation`、`PSStartTaskInformation`、`PSSubtaskInformation` 和 `PSTaskExecutionInformation` 上的 `SchedulingError` 屬性重新命名為 `FailureInformation`。
  - `FailureInformation` 會在每次工作失敗時傳回。 這包括所有先前排程的錯誤案例和非零工作結束代碼，以及新輸出檔案功能中的檔案上傳失敗情形。
  - 此結構與之前相同，因此使用此類型時，不需要變更任何程式碼。

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

額外受到影響的屬性如下：Get-AzureBatchPool、Get-AzureBatchSubtask 和 Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - 移除 `TargetDedicated`，並以 `TargetDedicatedComputeNodes` 和 `TargetLowPriorityComputeNodes` 加以取代。
 - `TargetDedicatedComputeNodes` 有別名：`TargetDedicated`。

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

這也會影響：Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - 將 `PSCloudPool` 上的 `TargetDedicated` 和 `CurrentDedicated` 屬性重新命名為 `TargetDedicatedComputeNodes` 和 `CurrentDedicatedComputeNodes`。

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a>**PSCloudPool 類型**

- 已將 `PSCloudPool` 上的 `ResizeError` 重新命名為 `ResizeErrors`，其現在是集合。

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- 已將 `PSPoolSpecification` 上的 `TargetDedicated` 屬性重新命名為 `TargetDedicatedComputeNodes`。

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - 移除 `Name`，並以 `Path` 加以取代。
 - `Path` 有別名：`Name`。

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

這也會影響：Get-AzureBatchNodeFileContent、Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>**PSNodeFile** 類型

 - 已將 `PSNodeFile` 上的 `Name` 屬性重新命名為 `Path`。

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- `PSSubtaskInformation` 的 `PreviousState` 和 `State` 屬性已不再屬於 `TaskState` 類型，而是屬於 `SubtaskState` 類型。
  - 不同於 `TaskState`，`SubtaskState` 沒有 `Active` 值，因為子工作不可能處於 `Active` 狀態。

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Compute Cmdlet 的重大變更

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- PSCredential 將取代 "UserName" 和 "Password" 參數

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>EventHub Cmdlet 的重大變更

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- 'New-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'New-AzureRmEventHubAuthorizationRule' Cmdlet

### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- 'Get-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Get-AzureRmEventHubAuthorizationRule' Cmdlet

### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- 'Set-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Set-AzureRmEventHubAuthorizationRule' Cmdlet

### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- 'Remove-AzureRmEventHubNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Remove-AzureRmEventHubAuthorizationRule' Cmdlet

### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- 'New-AzureRmEventHubNamespaceKey' Cmdlet 已移除。 請使用 'New-AzureRmEventHubKey' Cmdlet

### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- 'Get-AzureRmEventHubNamespaceKey' Cmdlet 已移除。 請使用 'Get-AzureRmEventHubKey' Cmdlet

### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- 'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- 'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Get-AzureRmEventHubNamespace <parameters>
```

### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- 'Status' 和 'Enabled' 屬性將會從 NamespceAttributes 中移除。

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property
$namespace = Set-AzureRmEventHubNamespace <parameters>
```

### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- 'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- 'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```

### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- 'EventHubPath' 屬性將會從 ConsumerGroupAttributes 中移除。

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Insights Cmdlet 的重大變更

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- **Add-AzureRMLogAlertRule** Cmdlet 已受到取代
- 10 月 1 日之後，使用此 Cmdlet 將不再有任何效果，因為這項功能將轉換為活動記錄警示。 請參閱 https://aka.ms/migratemealerts 以取得詳細資訊。

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- **Get-AzureRMUsage** Cmdlet 已受到取代

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- 輸出變更：來自 EventData 物件的 EventChannels 欄位 (由這些 Cmdlet 所傳回) 已受到取代，因為物件現在會傳回常數值 (Admin、Operation)。

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- 輸出變更：此 Cmdlet 的輸出會經過壓平合併 (也就是刪除屬性欄位)，進而改善使用者體驗。

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled

    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- 輸出變更：AutoscaleSettingResourceName 欄位將受到取代，因為它一律等於 Name 欄位。

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting

# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- 輸出變更：輸出類型會變更為傳回單一物件，其中包含要求識別碼和狀態碼。

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a>Network Cmdlet 的重大變更

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Resources Cmdlet 的重大變更

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- SecureString 將取代 "Password" 參數

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>ServiceBus Cmdlet 的重大變更

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- 'Get-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- 'Get-AzureRmServiceBusTopicKey' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusKey' Cmdlet。

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- 'New-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- 'New-AzureRmServiceBusTopicKey' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusKey' Cmdlet。

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- 'Remove-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。 請使用 'Remove-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- 'Set-AzureRmServiceBusTopicAuthorizationRule' Cmdlet 已移除。 請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- 'New-AzureRmServiceBusNamespaceKey' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusKey' Cmdlet。

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- 'Get-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- 'Get-AzureRmServiceBusQueueKey' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusKey' Cmdlet。

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- 'New-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- 'New-AzureRmServiceBusQueueKey' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusKey' Cmdlet。

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- 'Remove-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。 請使用 'GRemove-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- 'Set-AzureRmServiceBusQueueAuthorizationRule' Cmdlet 已移除。 請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Get-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- 'Get-AzureRmServiceBusNamespaceKey' Cmdlet 已移除。 請使用 'Get-AzureRmServiceBusKey' Cmdlet。

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- 'New-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'New-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Remove-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- 'Set-AzureRmServiceBusNamespaceAuthorizationRule' Cmdlet 已移除。 請使用 'Set-AzureRmServiceBusAuthorizationRule' Cmdlet。

### <a name="type-namespaceattributes"></a>**NamespaceAttributes 類型**
- 下列屬性已移除
    - 啟用
    - 狀態

```powershell-interactive
# Old
# The $namespace has Status and Enabled property
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a>**QueueAttribute 類型**
- 下列屬性會標示為已淘汰：
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
```

### <a name="type-topicattribute"></a>**TopicAttribute 類型**
- 下列屬性會標示為已淘汰：
    - Location
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$topic = Get-AzureRmServiceBusTopic <parameters>
```

### <a name="type-subscriptionattribute"></a>**SubscriptionAttribute 類型**
- 下列屬性會標示為已淘汰
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Location

```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
```
