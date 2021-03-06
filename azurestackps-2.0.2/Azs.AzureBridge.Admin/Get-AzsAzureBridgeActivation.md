---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d47f93addf05af19b523db6ba454443af2c34f
ms.sourcegitcommit: 5fcf17330d6f335561640a5ee3d98c59f7baab94
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/26/2020
ms.locfileid: "93968769"
---
# Get-AzsAzureBridgeActivation

## 摘要
傳回 Azure 橋接器啟用。

## 句法

###  (預設) 清單
```
Get-AzsAzureBridgeActivation -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### 獲取
```
Get-AzsAzureBridgeActivation -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### ResourceId
```
Get-AzsAzureBridgeActivation -ResourceId <String> [<CommonParameters>]
```

## 說明
在註冊 Azure 堆疊之後，啟用物件就會包含將 Azure 堆疊部署連結至 Azure 中的註冊（例如註冊到期日、名稱等）的資訊。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsAzureBridgeActivation -ResourceGroupName 'activationRG'
```

取得資源群組「activationRG」下的 Azure 橋接器啟用清單

### --------------------------範例 2--------------------------
```
Get-AzsAzureBridgeActivation -Name 'myActivation' -ResourceGroupName 'activationRG'
```

透過 [activationRG] 底下的名稱 "myActivation" 取得 Azure 橋接器啟用

## 參數

### -名稱
啟用的名稱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
在註冊 Azure 堆疊期間使用的資源群組;您也可以在入口網站中查看資源群組的名稱。

```yaml
Type: System.Management.Automation.PSObject
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
Type: System.Management.Automation.PSObject
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

### AzureStack AzureBridge. ActivationResource （）

## 筆記

## 相關連結

