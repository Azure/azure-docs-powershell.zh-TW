---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967656"
---
# New-AzureStorSimpleAccessControlRecord

## 摘要
建立存取控制記錄。

## 句法

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**新的-AzureStorSimpleAccessControlRecord** Cmdlet 會建立存取控制記錄。
您可以使用 **AccessControlRecord** 物件來設定卷。

## 示例

### 範例1：建立 Access Controlaccess 控制項記錄，並等待 resultaccess 控制項
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

這個命令會為名為 Iqn10 的 iSCSI 啟動器建立名為 Acr10 的存取控制記錄。
這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。

### 範例2：建立 Access Controlaccess 控制項 recordaccess 控制項
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

這個命令會為名為 Iqn11 的 iSCSI 啟動器建立名為 Acr11 的存取控制記錄。
這個命令不會指定 *WaitForComplete* 參數，因此，命令會啟動工作，然後傳回 **TaskResponse** 物件。
若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。

## 參數

### -ACRName
指定存取控制記錄的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IQNInitiatorName
指定此 Cmdlet 提供其存取權的 iSCSI 啟動器 (IQN) 的 iSCSI 限定名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

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

### TaskStatusInfo, TaskResponse
如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。
如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。

## 筆記

## 相關連結

[AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[移除-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


