---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452967"
---
# New-AzureRmSubscriptionDefinition

## 摘要
建立訂閱定義。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 建立訂閱定義
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## 說明
**新的-AzureRmSubscriptionDefinition** Cmdlet 會建立訂閱定義。

## 示例

### 範例1
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

使用預設訂閱顯示名稱建立訂閱定義。

### 範例2
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

使用自訂訂閱顯示名稱建立訂閱定義。

## 參數

### -名稱
要建立之訂閱定義的名稱。

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

### -OfferType
建立基礎訂閱時要使用的優惠類型。

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

### -SubscriptionDisplayName
建立訂閱定義的基礎訂閱時所要使用的顯示名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSSubscriptionDefinition 中的 SubscriptionDefinition。

## 筆記

## 相關連結

