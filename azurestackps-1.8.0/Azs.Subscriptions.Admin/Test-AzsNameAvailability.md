---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793446"
---
# Test-AzsNameAvailability

## 摘要
傳回指定訂閱資源類型和名稱的 avaialbility

## 句法

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## 說明
傳回指定訂閱資源類型和名稱的 avaialbility

## 示例

### --------------------------範例 1--------------------------
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

傳回指定訂閱資源類型和名稱的 avaialbility

## 參數

### -名稱
要驗證的資源名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
要驗證的資源類型。

```yaml
Type: String
Parameter Sets: (All)
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

### AzureStack CheckNameAvailabilityResponse 的訂閱。

## 筆記

## 相關連結

