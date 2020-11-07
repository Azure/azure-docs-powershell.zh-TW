---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1f3a965d287aa266683636b4b17a8d8954cace8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793215"
---
# Get-AzsBackupConfiguration

## 摘要
傳回備份配置清單。

## 句法

###  (預設) 清單
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 獲取
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## 說明
傳回備份配置清單。

## 示例

### 範例1
```
Get-AzsBackupConfiguration
```

取得 Azure 堆疊備份設定。

## 參數

### -位置
備份位置。

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -上方
傳回參數值所指定的前 N 個專案。
在-Skip 參數後套用。

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -略過
略過參數值所指定的前 N 個專案。

```yaml
Type: System.Int32
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

### BackupLocation 中的 [AzureStack]

## 筆記

## 相關連結
