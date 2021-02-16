---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134110"
---
# Get-AzMigrateJob

## 摘要
檢索 Azure 遷移工作的狀態。

## 句法

### ListByName (預設) 
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 說明
Get-AzMigrateJob Cmdlet 會 retrives Azure 遷移作業的狀態。

## 示例

### 範例1：根據作業 Id 取得
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

這會透過其識別碼來檢索作業。

### 範例2：依資源群組和專案列出清單
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

這會取得專案中的所有作業。

### 範例3：依資源群組、專案與工作名稱取得
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

這會取得特定作業。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -篩選
OData 篩選選項。

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
指定複製伺服器的工作物件。
若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -作業 Id
指定需要檢索其詳細資料的作業 id。

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
作業識別碼

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
指定要在其中複製伺服器的 Azure 遷移專案。

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -專案名稱
[遷移專案] 的名稱。

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
指定目前訂閱中 Azure 遷移專案的資源群組。

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
[恢復服務] 電子倉庫所在之資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 訂閱 ID。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### IJob 中的 Api20180110 （）。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IJob> ：指定複製伺服器的工作物件。
  - `[Location <String>]`：資源位置
  - `[ActivityId <String>]`：活動識別碼。
  - `[AllowedAction <String[]>]`：允許對作業執行的動作。
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`：受影響的物件屬性（例如來源伺服器、來源雲端、目標伺服器、目標雲端等）都是以工作流程物件詳細資料為基礎。
    - `[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。
  - `[EndTime <DateTime?>]`：結束時間。
  - `[Error <IJobErrorDetails[]>]`：錯誤。
    - `[CreationTime <DateTime?>]`：作業錯誤的建立時間。
    - `[ErrorLevel <String>]`：錯誤等級錯誤。
    - `[ProviderErrorDetailErrorCode <Int32?>]`：錯誤代碼。
    - `[ProviderErrorDetailErrorId <String>]`：提供者錯誤 Id。
    - `[ProviderErrorDetailErrorMessage <String>]`：錯誤訊息。
    - `[ProviderErrorDetailPossibleCaus <String>]`：錯誤的可能原因。
    - `[ProviderErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。
    - `[ServiceErrorDetailActivityId <String>]`： [活動識別碼]。
    - `[ServiceErrorDetailCode <String>]`：錯誤代碼。
    - `[ServiceErrorDetailMessage <String>]`：錯誤訊息。
    - `[ServiceErrorDetailPossibleCaus <String>]`：錯誤的可能原因。
    - `[ServiceErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。
    - `[TaskId <String>]`：任務的識別碼。
  - `[FriendlyName <String>]`： DisplayName。
  - `[ScenarioName <String>]`： ScenarioName。
  - `[StartTime <DateTime?>]`：開始時間。
  - `[State <String>]`：工作的狀態。 它是下列其中一個值，例如 NotStarted、InProgress、成功、失敗、取消、暫停或其他。
  - `[StateDescription <String>]`：作業狀態的描述。 例如，對於 [成功] 狀態，說明可以是已完成、PartiallySucceeded、CompletedWithInformation 或略過。
  - `[TargetInstanceType <String>]`：受影響之物件的類型，屬於 {Microsoft.Azure.SiteRecovery.V2015_11_10 AffectedObjectType} 類別。
  - `[TargetObjectId <String>]`：受影響的物件識別碼。
  - `[TargetObjectName <String>]`：受影響物件的名稱。
  - `[Task <IAsrTask[]>]`： [任務]。
    - `[AllowedAction <String[]>]`：適用于此任務的狀態/動作。
    - `[CustomDetailInstanceType <String>]`：任務詳細資料的類型。
    - `[EndTime <DateTime?>]`：結束時間。
    - `[Error <IJobErrorDetails[]>]`：任務錯誤詳細資料。
    - `[FriendlyName <String>]`：名稱。
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`：子任務。
    - `[GroupTaskCustomDetailInstanceType <String>]`：任務詳細資料的類型。
    - `[Name <String>]`：唯一任務名稱。
    - `[StartTime <DateTime?>]`：開始時間。
    - `[State <String>]`： [狀態]。 它是下列其中一個值，例如 NotStarted、InProgress、成功、失敗、取消、暫停或其他。
    - `[StateDescription <String>]`：任務狀態的描述。 例如，如果成功的狀態，說明可以是已完成、PartiallySucceeded、CompletedWithInformation 或略過。
    - `[TaskId <String>]`：識別碼。
    - `[TaskType <String>]`：任務類型。 CustomDetails 屬性中的詳細資料視這種類型而定。

## 相關連結

