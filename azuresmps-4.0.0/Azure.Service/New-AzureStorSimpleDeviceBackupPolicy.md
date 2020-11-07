---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967654"
---
# New-AzureStorSimpleDeviceBackupPolicy

## 摘要
建立備份原則。

## 句法

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**新的-AzureStorSimpleDeviceBackupPolicy** Cmdlet 會建立備份原則。
備份原則包含一或多個可以在一或多個卷上執行的備份排程。
若要建立備份排程，請使用 **AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet。

## 示例

### 範例1：建立備份原則
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

第一個命令會使用 **新的 AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet 來建立備份排程設定物件，然後將該物件儲存在 $Schedule 01 變數中。

第二個命令會使用 **新的 AzureStorSimpleDeviceBackupScheduleAddConfig** 建立另一個備份設定物件，然後將該物件儲存在 $Schedule 02 變數中。

第三個命令會建立一個名為 $ScheduleArray 的空陣列變數。
接下來的兩個命令會將在前兩個命令中建立的物件新增到 $ScheduleArray。

第六個命令會使用 **AzureStorSimpleDeviceVolumeContainer** Cmdlet，透過名為 Contoso63-AppVm 的裝置取得體積容器，然後將該容器物件儲存在 $DeviceContainer 變數中。

第七個命令會使用 **AzureStorSimpleDeviceVolume** Cmdlet 來取得儲存在 $DeviceContainer 第一個成員中之卷容器的體積，然後將該體積條儲存在 $Volume 變數中。

第八個命令會建立一個名為 $VolumeArray 的空陣列變數。
下一個命令會將卷識別碼新增到 $VolumeArray。
此值會識別儲存在備份原則執行之 $Volume 的音量。
您可以將其他卷識別碼新增至 $VolumeArray。

最終命令會針對名為 Contoso63-AppVm 的裝置建立名為 GeneralPolicy07 的備份原則。
此命令會指定儲存在 $ScheduleArray 中的排程設定物件。
此命令會指定 $VolumeArray 中要套用原則的量或體積。
您可以使用 **AzureStorSimpleDeviceBackupPolicy** Cmdlet 來驗證備份原則。

## 參數

### -BackupPolicyName
指定備份原則的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupSchedulesToAdd
指定要新增至原則的 **BackupScheduleBase** 物件陣列。
每個物件代表排程。
備份原則包含一或多個排程。
若要取得 **BackupScheduleBase** 物件，請使用 **AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet。

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
指定要建立備份原則之 StorSimple 裝置的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定 Azure 設定檔。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeIdsToAdd
指定要新增至備份原則之卷識別碼的陣列。

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### BackupPolicy
這個 Cmdlet 會傳回包含新排程和卷的 **BackupPolicy** 物件。

## 筆記

## 相關連結

[AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[移除-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[新-AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)


