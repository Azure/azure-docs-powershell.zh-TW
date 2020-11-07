---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793340"
---
# Stop-AzsScaleUnitNode

## 摘要
關閉刻度單位節點的電源。

## 句法

### 停止 (預設) 
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceId
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
關閉刻度單位節點的電源。

## 示例

### --------------------------範例 1--------------------------
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

關閉 [縮放單位] 節點。

### --------------------------範例 2--------------------------
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

關閉比例單位節點的電源。

## 參數

### -AsJob
執行非同步作業，然後傳回工作物件。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
不要要求確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
資源的位置。

```yaml
Type: String
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
[縮放單位] 節點的名稱。

```yaml
Type: String
Parameter Sets: Stop
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
Parameter Sets: Stop
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
縮放單位節點資源識別碼。

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

### -關閉
如果設定正常關閉 [縮放單位] 節點，否則請關閉 [縮放單位] 節點的電源。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
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

## 筆記

## 相關連結

