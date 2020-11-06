---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmImage.md
ms.openlocfilehash: 3976418d89076b290500343775ca42e2fb975659
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449946"
---
# Get-AzureRmImage

## 摘要
取得影像的屬性。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmImage [[-ResourceGroupName] <String>] [[-ImageName] <String>] [[-Expand] <String>]
 [<CommonParameters>]
```

## 說明
**AzureRmImage** Cmdlet 會取得影像的屬性。

## 示例

### 範例1
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01'
```

這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Image01 ' 的影像的屬性。

### 範例2
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01'
```

這個命令會取得資源群組 ' ResourceGroup01 ' 中所有影像的屬性。

### 範例3
```
PS C:\> Get-AzureRmImage
```

這個命令會取得訂閱下所有影像的屬性。

## 參數

### -展開
指定 [擴大運算式] 查詢。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageName
指定影像的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### System.object

## 筆記

## 相關連結

