---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793159"
---
# Get-AzsLogicalSubnet

## 摘要
傳回所有邏輯子網的清單。

## 句法

###  (預設) 清單
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 獲取
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## 說明
傳回所有邏輯子網的清單。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

取得指定邏輯網路和位置的所有邏輯子網清單。

### --------------------------範例 2--------------------------
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

根據名稱取得指定之邏輯網路和位置的特定邏輯子網。

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

### -位置
資源的位置。

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogicalNetwork
邏輯網路的名稱。

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
邏輯子網的名稱。

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
已註冊資源提供者的資源群組。

```yaml
Type: String
Parameter Sets: List, Get
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

### LogicalSubnet 中的 AzureStack （）

## 筆記

## 相關連結

