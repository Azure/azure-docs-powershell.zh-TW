---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448035"
---
# Remove-AzureRmRecoveryServicesAsrPolicy

## 摘要
從 [恢復服務] 保存庫刪除指定的 ASR 複製原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrPolicy** Cmdlet 已從復原服務保存庫中刪除指定的複製原則。

## 示例

### 範例1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

開始刪除指定的複製原則，並傳回用於追蹤操作的 ASR 作業。

## 參數

### -InputObject
Cmdlet 的輸入物件：與要刪除之複製原則相對應的 ASR 複製原則物件。

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### RecoveryServices. SiteRecovery. ASRPolicy

## 輸出

### System.object

## 筆記

## 相關連結

[AzureRmRecoveryServicesAsrPolicy](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[新-AzureRmRecoveryServicesAsrPolicy](./New-AzureRmRecoveryServicesAsrPolicy.md)
