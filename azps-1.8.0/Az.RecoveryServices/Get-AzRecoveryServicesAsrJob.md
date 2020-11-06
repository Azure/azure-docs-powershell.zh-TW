---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621189"
---
# Get-AzRecoveryServicesAsrJob

## 摘要
取得所指定 ASR 作業的詳細資料，或 [復原服務] 保存庫中最近的 ASR 作業清單。

## 句法

### ByParam (預設) 
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzRecoveryServicesAsrJob** Cmdlet 會取得 Azure 網站恢復作業。
您可以使用此 Cmdlet 來查看 [復原服務] 保存庫中的 ASR 作業。

## 示例

### 範例1
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

傳回特定 ASR 物件上的所有工作 (參照 ASR 物件（例如複製的專案或復原方案的識別碼）。 )  

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
指定作業的結束時間。
這個 Cmdlet 會取得在指定時間之前所啟動的所有作業。
若要取得此參數的 **DateTime** 物件，請使用 Get-Date Cmdlet。
如需詳細資訊，請輸入 `Get-Help Get-Date` 。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -工作
指定要取得更新詳細資料的 ASR 工作物件。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
依名稱指定 ASR 作業。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定作業的開始時間。
這個 Cmdlet 會取得在指定時間之後所啟動的所有作業。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
指定 ASR 作業的狀態。
這個 Cmdlet 會取得符合指定狀態的所有作業。
此參數可接受的值為：

- NotStarted
- 正在
- 成功
- 換句話說
- 成功
- 取消
- 封存

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetObjectId
指定物件的識別碼。 用來搜尋指定物件上的工作。

```yaml
Type: System.String
Parameter Sets: ByParam
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

### RecoveryServices. SiteRecovery. ASRJob

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

[重新開機-AzRecoveryServicesAsrJob](./Restart-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[停止 AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
