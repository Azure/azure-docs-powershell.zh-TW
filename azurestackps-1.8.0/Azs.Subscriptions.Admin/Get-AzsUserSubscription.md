---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793649"
---
# Get-AzsUserSubscription

## 摘要
以系統管理員身分取得使用者訂閱清單。

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
以系統管理員身分取得使用者訂閱清單。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsUserSubscription
```

以系統管理員身分取得使用者訂閱清單。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AzureStack. 系統管理. 訂閱

## 筆記

## 相關連結

