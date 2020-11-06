---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMImage.md
ms.openlocfilehash: f9e8eb9441604e3c07453f1e387ba17bd4623d55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446383"
---
# Get-AzureRmVMImage

## 摘要
取得 VMImage 的所有版本。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ListVMImage
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [<CommonParameters>]
```

### GetVMImageDetail
```
Get-AzureRmVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [<CommonParameters>]
```

## 說明
**AzureRmVMImage** Cmdlet 會取得 VMImage 的所有版本。

## 示例

### 範例1：取得 VMImage 物件
```
PS C:\> Get-AzureRmVMImage -Location "Central US" -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.04-DAILY"
```

這個命令會取得符合指定值的所有 VMImage 版本。

## 參數

### -FilterExpression
指定篩選運算式。

```yaml
Type: String
Parameter Sets: ListVMImage
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定 VMImage 的位置。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -優惠
指定 VMImage 產品類型。
若要取得影像優惠，請使用 Get-AzureRmVMImageOffer Cmdlet。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublisherName
指定 VMImage 的發行者。
若要取得影像發行商，請使用 Get-AzureRmVMImagePublisher Cmdlet。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
指定 VMImage SKU。
若要取得 SKU，請使用 Get-AzureRmVMImageSku Cmdlet。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -版本
指定 VMImage 的版本。

```yaml
Type: String
Parameter Sets: GetVMImageDetail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[儲存-AzureRmVMImage](./Save-AzureRmVMImage.md)


