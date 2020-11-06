---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: ac3f3c843f13fd500156cf148b5c80436e2e2649
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453327"
---
# Resume-AzureRmRecoveryServicesAsrJob

## 摘要
繼續已暫停的 Azure 網站還原作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByObject (預設) 
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**Resume AzureRmRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。

## 示例

### 範例1
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

如果指定的工作處於 [等待] 或 [暫停] 狀態，並傳回對應至 ASR 作業的更新 ASR 工作物件，請繼續執行該作業。

## 參數

### -批註
作業記錄的批註。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Cmdlet 的輸入物件：對應至要繼續作業的 ASR 工作物件。

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
依名稱指定 ASR 作業。

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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

[AzureRmRecoveryServicesAsrJob](./Get-AzureRmRecoveryServicesAsrJob.md)

[重新開機-AzureRmRecoveryServicesAsrJob](./Restart-AzureRmRecoveryServicesAsrJob.md)

[停止 AzureRmRecoveryServicesAsrJob](./Stop-AzureRmRecoveryServicesAsrJob.md)
