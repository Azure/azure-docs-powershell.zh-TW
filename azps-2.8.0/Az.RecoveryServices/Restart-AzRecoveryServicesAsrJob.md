---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: c53cc7b410f0898af7a643babef1781433cbd120
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792341"
---
# Restart-AzRecoveryServicesAsrJob

## 摘要
重新開機 Azure Site Recovery 作業。

## 句法

### ByObject (預設) 
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**Restart AzRecoveryServicesAsrJob** Cmdlet 會重新開機 Azure Site Recovery 作業。

## 示例

### 範例1
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

重新開機指定的 ASR 作業，並傳回 ASR 作業的更新 ASR 工作物件。

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

### -InputObject
Cmdlet 的輸入物件：與要重新開機之 ASR 作業對應的 ASR 工作物件


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
依名稱指定作業。

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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[AzRecoveryServicesAsrJob](./Get-AzRecoveryServicesAsrJob.md)

[Resume-AzRecoveryServicesAsrJob](./Resume-AzRecoveryServicesAsrJob.md)

[停止 AzRecoveryServicesAsrJob](./Stop-AzRecoveryServicesAsrJob.md)
