---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443035"
---
# Get-AzsGalleryItem

## 摘要
列出圖庫專案。

## 句法

###  (預設) 清單
```
Get-AzsGalleryItem [<CommonParameters>]
```

### 獲取
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## 說明
取得 Azure 堆疊 Marketplace 中可用的圖庫專案清單

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsGalleryItem
```

清單庫專案。

### --------------------------範例 2--------------------------
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

依名稱取得圖庫專案。

## 參數

### -名稱
圖庫專案的身分識別。
包括發行者名稱、專案名稱，並且可能包含以句點字元分隔的版本。

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AzureStack （系統管理）。

## 筆記

## 相關連結

