---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623243"
---
# Get-AzsUserSubscription

## 摘要
取得使用者訂閱清單做為操作員。

## 句法

###  (預設) 清單
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### 獲取
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## 說明
取得使用者訂閱清單做為操作員。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsUserSubscription
```

取得使用者訂閱清單做為操作員。

## 參數

### -篩選
OData 篩選參數。

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
[訂閱識別碼] 參數。

```yaml
Type: Guid
Parameter Sets: Get
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

## 輸出

### AzureStack. 系統管理. 訂閱

## 筆記

## 相關連結

