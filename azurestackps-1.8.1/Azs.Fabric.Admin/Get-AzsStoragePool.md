---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793835"
---
# Get-AzsStoragePool

## 摘要
傳回某個位置的所有儲存空間池清單。

## 句法

###  (預設) 清單
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 獲取
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### ResourceId
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## 說明
傳回某個位置的所有儲存空間池清單。

## 示例

### 範例1
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

取得指定位置的所有儲存空間池。

### 範例2
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

在指定的位置取得儲存池名稱的儲存空間池。

## 參數

### -名稱
儲存空間池名稱。

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

### -It
儲存空間子系統的名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### StoragePool 中的 AzureStack （）

## 筆記

## 相關連結
