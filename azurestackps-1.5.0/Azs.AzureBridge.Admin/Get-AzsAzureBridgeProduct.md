---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16649f3f935a488bb6f5913e393f9628e7f26aa7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/22/2020
ms.locfileid: "93457727"
---
# Get-AzsAzureBridgeProduct

## 摘要
傳回可從 Azure Marketplace 下載的產品清單。

## 句法

###  (預設) 清單
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### 獲取
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### ResourceId
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## 說明
傳回可從 Azure Marketplace 下載的產品清單。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

取得可從 Azure Marketplace 下載的產品清單。

### --------------------------範例 2--------------------------
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

取得從 Azure Marketplace 透過名稱下載的產品資訊。

## 參數

### -ActivationName
啟用的名稱。

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
產品名稱。

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源所在的資源群組。

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
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

### -略過
略過參數值所指定的前 N 個專案。

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -上方
傳回參數值所指定的前 N 個專案。
在-Skip 參數後套用。

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AzureStack AzureBridge. ProductResource （）

## 筆記

## 相關連結

