---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793409"
---
# Set-AzsSubscription

## 摘要
建立或更新訂閱。

## 句法

### 設定 (預設) 
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceId
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
建立或更新訂閱。

## 示例

### --------------------------範例 1--------------------------
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

建立或更新訂閱。

## 參數

### -DisplayName
訂閱名稱。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Posbbily 由 AzsNetworkQuota 傳回的已修改網路配額。

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -位置
資源所在位置的位置。

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfferId
受委派提供者範圍內提供的識別碼。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
[資源識別碼]。

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
訂閱狀態。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
[訂閱識別碼]。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -標記
索引鍵/值對清單。

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
目錄租使用者識別碼。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -類型
資源類型。

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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

## 輸出

### AzureStack. SubscriptionModel 的 [訂閱]。

## 筆記

## 相關連結

