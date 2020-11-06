---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 05fc2025b8023708f17b3494cd5568f13503eee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453331"
---
# Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping

## 摘要
刪除指定的 ASR 儲存分類對應。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet 會刪除指定的 Azure Site Recovery 儲存分類對應。

## 示例

### 範例1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

開始刪除指定的儲存分類對應，並傳回用於追蹤操作的 ASR 作業。

## 參數

### -InputObject
Cmdlet 的輸入物件：與要刪除之 ASR 儲存分類對應的 ASR 儲存分類對應物件。

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

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

### RecoveryServices. SiteRecovery. ASRStorageClassificationMapping

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

[AzureRmRecoveryServicesAsrStorageClassificationMapping](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[新-AzureRmRecoveryServicesAsrStorageClassificationMapping](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
