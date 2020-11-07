---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967004"
---
# Get-AzureStorSimpleJob

## 摘要
取得 StorSimple 作業。

## 句法

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureStorSimpleJob** Cmdlet 會取得 Azure StorSimple 作業。
指定實例識別碼以取得特定作業。
指定其他參數，以限制此 Cmdlet 取得的作業。

這個 Cmdlet 會傳回200工作的最大值。
如果有超過200個作業，請使用 *第一個* 和 [ *略過* ] 參數來取得剩餘作業。
如果您為 *Skip* 指定的值是100，而 *第一次* 則是50，則此 Cmdlet 不會傳回第一個100結果。
它會在跳過的100之後傳回接下來的50結果。

## 示例

### 範例1：使用識別碼來取得作業
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

這個命令會取得具有指定識別碼之作業的資訊。

### 範例2：使用裝置名稱取得工作
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

這個命令會取得名為 8600-Bravo 001 之裝置工作的相關資訊。
此命令會取得裝置的前兩個作業。

### 範例3：取得完成的工作
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

這個命令會取得已完成的工作。
命令在跳過前十個作業之後，只會取得前兩個作業。

### 範例4：取得手動備份作業
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

這個命令會取得手動備份類型的作業。

### 範例5：在指定的時間之間取得作業
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

前兩個命令會使用 Get-Date Cmdlet 來建立 **DateTime** 物件。
這些命令會將新的時間儲存在 $StartTime，並 $EndTime 變數中。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。

最終命令會在 $StartTime 和 $EndTime 中所儲存的時間之間，取得名為 Device07 之裝置的工作。

## 參數

### -DeviceName
指定 StorSimple 裝置的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -優先
只取得指定數目的物件。
輸入要取得的物件數目。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -從
指定此 Cmdlet 取得作業的開始日期和時間。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
指定要取得的作業識別碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -略過
忽略指定的物件數目，然後取得剩餘的物件。
輸入要略過的物件數目。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定狀態。
此參數可接受的值為：

- 進行
- 完畢
- 取消
- 成功
- 取消
- CompletedWithErrors

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
指定此 Cmdlet 取得作業的結束日期和時間。

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -類型
指定作業類型。
此參數可接受的值為：

- 備份
- ManualBackup
- 還原
- CloneWorkflow
- DeviceRestore
- 時更新
- SupportPackage
- VirtualApplianceProvisioning

```yaml
Type: String
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
您無法將輸入管到這個 Cmdlet。

## 輸出

### IList \<DeviceJobDetails\> 、DeviceJobDetails
這個 Cmdlet 會傳回作業詳細資料物件的清單，或者，如果您指定 *InstanceID* 參數，則會傳回單一作業詳細資料物件。

## 筆記

## 相關連結

[停止 AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)


