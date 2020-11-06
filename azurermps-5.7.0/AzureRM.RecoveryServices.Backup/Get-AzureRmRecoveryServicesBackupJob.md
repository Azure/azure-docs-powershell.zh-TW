---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 5e6555095563fd5c0589835b28ad293f395fffaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446140"
---
# Get-AzureRmRecoveryServicesBackupJob

## 摘要
取得備份作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesBackupJob** Cmdlet 會針對特定的電子倉庫取得 Azure 備份作業。

使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。

## 示例

### 範例1：取得所有進行中的工作
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

第一個命令會以陣列形式取得進行中作業的狀態，然後將它儲存在 $Joblist 變數中。

第二個命令會顯示 $Joblist 陣列中的第一個專案。

### 範例2：在過去7天內取得所有失敗的工作
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

此命令會從 vault 中的最後一周取得失敗的工作。
*From* 參數指定過去在 UTC 中指定的時間（以七天為單位）。
該命令不會指定 *To* 參數的值。
因此，它會使用目前時間的預設值。

### 範例3：取得進行中的工作並等待完成
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。

## 參數

### -BackupManagementType
指定備份管理類型。
目前僅支援 Add-azurevm。

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -從
指定此 Cmdlet 所取得作業之時間範圍的開始（以 **DateTime** 物件）。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。
如需 **DateTime** 物件的詳細資訊，請輸入 `Get-Help Get-Date` 。
針對日期使用 UTC 格式。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -工作
指定要取得的備份作業名稱。

```yaml
Type: JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -作業 Id
指定此 Cmdlet 所取得作業的識別碼。
識別碼是 **AzureRmRecoveryServicesBackupJob** 物件的 InstanceId 屬性。
若要取得 **AzureRmRecoveryServicesBackupJob** 物件，請使用 AzureRmRecoveryServicesBackupJob。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -操作
指定此 Cmdlet 取得作業的操作。
此參數可接受的值為：

- 備份
- ConfigureBackup
- DeleteBackupData
- 註冊表
- 還原
- 對
- 登出

```yaml
Type: JobOperation
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定此 Cmdlet 取得作業的狀態。
此參數可接受的值為：

- 正在
- 成功
- 取消
- 正在
- 完畢
- CompletedWithWarnings

```yaml
Type: JobStatus
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
指定此 Cmdlet 所取得作業之時間範圍的結尾（作為 **DateTime** 物件）。
預設值為目前的系統時間。
如果您指定此參數，您也必須指定 *From* 參數。
針對日期使用 UTC 格式。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### JobBase 中的 RecoveryServices，然後再

### [System.object]. RecoveryServices [JobBase] 的 [] （.]）

## 筆記

## 相關連結

[AzureRmRecoveryServicesBackupJobDetails](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[停止 AzureRmRecoveryServicesBackupJob](./Stop-AzureRmRecoveryServicesBackupJob.md)

[稍候-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


