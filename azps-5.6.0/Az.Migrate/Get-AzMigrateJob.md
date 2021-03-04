---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: 9521e069f0b472353403a16caffad86e1147c1fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909661"
---
# Get-AzMigrateJob

## 簡介
會取回 Azure Migrate 工作的狀態。

## 語法

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

## 描述
此Get-AzMigrateJob Cmdlet 會重新重試 Azure Migrate 工作的狀態。

## 例子

### 範例 1：取得工作識別碼
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

這會以識別碼來取回工作。

### 範例 2：按資源群組和專案列出
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

這會獲得專案中的所有工作。

### 範例 3：取得資源群組、專案和工作名稱
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

這會獲得特定工作。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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
若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。

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

### -JobID
指定需要取回詳細資料的工作識別碼。

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
工作識別碼

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
指定要複製伺服器的 Azure Migrate Project。

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

### -ProjectName
此為遷移專案的名稱。

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
指定目前訂閱中 Azure Migrate Project 的資源群組。

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
復原服務庫存在之資源組的名稱。

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
Azure 訂閱識別碼。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

## 輸出

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## 筆記

別名

複雜的參數屬性

若要建立下列描述的參數，請建構包含適當屬性的雜湊表。 有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。


INPUTOBJECT： <IJob> 指定複製伺服器的工作物件。
  - `[Location <String>]`：資源位置
  - `[ActivityId <String>]`：活動識別碼。
  - `[AllowedAction <String[]>]`：工作的允許動作。
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`：根據工作流程物件詳細資料，受影響的物件屬性，例如來源伺服器、來源雲端、目標伺服器、目標雲端等。
    - `[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。
  - `[EndTime <DateTime?>]`：結束時間。
  - `[Error <IJobErrorDetails[]>]`：錯誤。
    - `[CreationTime <DateTime?>]`：工作錯誤的建立時間。
    - `[ErrorLevel <String>]`：錯誤層級錯誤。
    - `[ProviderErrorDetailErrorCode <Int32?>]`：錯誤碼。
    - `[ProviderErrorDetailErrorId <String>]`：提供者錯誤 ID。
    - `[ProviderErrorDetailErrorMessage <String>]`：錯誤訊息。
    - `[ProviderErrorDetailPossibleCaus <String>]`：此錯誤的可能原因。
    - `[ProviderErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。
    - `[ServiceErrorDetailActivityId <String>]`：活動識別碼。
    - `[ServiceErrorDetailCode <String>]`：錯誤碼。
    - `[ServiceErrorDetailMessage <String>]`：錯誤訊息。
    - `[ServiceErrorDetailPossibleCaus <String>]`：可能的錯誤原因。
    - `[ServiceErrorDetailRecommendedAction <String>]`：解決錯誤的建議動作。
    - `[TaskId <String>]`：任務的識別碼。
  - `[FriendlyName <String>]`：DisplayName。
  - `[ScenarioName <String>]`：ScenarioName。
  - `[StartTime <DateTime?>]`：開始時間。
  - `[State <String>]`：工作的狀態。 這是其中一個值 - 未啟動、InProgress、已成功、失敗、已取消、已暫停或其他。
  - `[StateDescription <String>]`：Job 狀態的描述。 例如-對於成功狀態，描述可以完成、部分完成、CompletedWithInformation 或略過。
  - `[TargetInstanceType <String>]`：受影響物件的類型為 {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} 類。
  - `[TargetObjectId <String>]`：受影響的物件識別碼。
  - `[TargetObjectName <String>]`：受影響物件的名稱。
  - `[Task <IAsrTask[]>]`：工作。
    - `[AllowedAction <String[]>]`：適用于此工作的狀態/動作。
    - `[CustomDetailInstanceType <String>]`：工作詳細資料的類型。
    - `[EndTime <DateTime?>]`：結束時間。
    - `[Error <IJobErrorDetails[]>]`：工作錯誤詳細資料。
    - `[FriendlyName <String>]`：名稱。
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`：子工作。
    - `[GroupTaskCustomDetailInstanceType <String>]`：工作詳細資料的類型。
    - `[Name <String>]`：唯一的工作名稱。
    - `[StartTime <DateTime?>]`：開始時間。
    - `[State <String>]`：狀態。 這是其中一個值 - 未啟動、InProgress、已成功、失敗、已取消、已暫停或其他。
    - `[StateDescription <String>]`：工作狀態的描述。 例如，對於成功狀態，描述可以是完成、部分Suced、CompletedWithInformation 或略過。
    - `[TaskId <String>]`：識別碼。
    - `[TaskType <String>]`：工作類型。 CustomDetails 屬性中的詳細資料取決於此類型。

## 相關連結

