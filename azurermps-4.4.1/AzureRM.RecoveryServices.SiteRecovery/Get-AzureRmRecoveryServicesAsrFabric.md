---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446695"
---
# Get-AzureRmRecoveryServicesAsrFabric

## 摘要
取得 Azure 網站恢復結構的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 預設 (預設) 
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrFabric** Cmdlet 會取得指定 Azure 網站復原結構的屬性，或在恢復服務電子倉庫中的所有 azure 網站復原結構。

## 示例

### 範例1
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

傳回保存庫中的所有 Azure Site Recovery 結構。

## 參數

### FriendlyName
依結構的易記名稱搜尋 ASR 結構。

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
透過結構的名稱搜尋 ASR 結構。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### [System.object]. 清單 ' 1 [RecoveryServices. SiteRecovery，ASRFabric，，RecoveryServices. SiteRecovery，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = null]]

## 筆記

## 相關連結

[新-AzureRmRecoveryServicesAsrFabric](./New-AzureRmRecoveryServicesAsrFabric.md)

[移除-AzureRmRecoveryServicesAsrFabric](./Remove-AzureRmRecoveryServicesAsrFabric.md)
