---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611766"
---
# Get-AzsDelegatedProvider

## 摘要
取得 delegatedProviders 清單。

## 句法

###  (預設) 清單
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### 獲取
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## 說明
取得 delegatedProviders 清單。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsDelegatedProvider
```

取得委派提供者的清單。

### --------------------------範例 2--------------------------
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

取得特定的委派提供者。

## 參數

### -DelegatedProviderId
DelegatedProvider 識別碼]。

```yaml
Type: Guid
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

### AzureStack. 系統管理. 訂閱

## 筆記

## 相關連結

