---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442767"
---
# Get-AzsNetworkAdminOverview

## 摘要
取得網路資源提供者狀態的概覽。

## 句法

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## 說明
取得網路資源提供者狀態的概覽。 個別屬性提供資源使用狀況的詳細計數，以及依元件進行健康情況。

## 示例

### --------------------------範例 1--------------------------
```
Get-AzsNetworkAdminOverview
```

取得網路系統管理員概覽。

### --------------------------範例 2--------------------------
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

取得公用 ip 位址使用量。

## 參數

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AdminOverview 中的 AzureStack 的管理

## 筆記

## 相關連結

