---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967542"
---
# Remove-AzureStorSimpleAccessControlRecord

## 摘要
從服務設定中刪除存取控制記錄。

## 句法

### IdentifyByName
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleAccessControlRecord** Cmdlet 會從服務設定中刪除存取控制記錄。

## 示例

### 範例1：移除 Access Controlaccess 控制項 recordaccess 控制項
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

這個命令會刪除名為 Acr10 的存取控制記錄。
這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。

### 範例2：使用 pipelineAccess Controlaccess Controlaccess 控制項移除 Access Controlaccess 控制項記錄
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

這個命令會使用 **AzureStorSimpleAccessControlRecord** 取得名為 Acr10 的 **AccessControlRecord** ，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。
命令會啟動移除 **AccessControlRecord** 物件的作業，然後傳回 **TaskResponse** 物件。
若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。

## 參數

### -ACR
指定要刪除的 **AccessControlRecord** 物件。
若要取得 **AccessControlRecord** 物件，請使用 **AzureStorSimpleAccessControlRecord** Cmdlet。

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
指定要刪除的存取控制記錄名稱。

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
表示此 Cmdlet 不會提示您進行確認。

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

### AccessControlRecord
這個 Cmdlet 接受 **AccessControlRecord** 物件。
**AccessControlRecord** 物件包含下欄欄位： 

- **GlobalId** ( **字串** )  
- **InitiatorName** ( **字串** )  
- **InstanceId** ( **字串** )  
- **名稱** ( **字串** )  
- **OperationInProgress** ( **OperationInProgress** )  
- **VolumeCount** ( **int** ) 

## 輸出

### TaskStatusInfo, TaskResponse
如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。
如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。

## 筆記

## 相關連結

[AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[新-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


