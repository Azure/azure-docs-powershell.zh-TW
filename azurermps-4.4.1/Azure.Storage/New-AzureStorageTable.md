---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 2f051fb0724ac266753d87fc30489398a4aa64a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447218"
---
# New-AzureStorageTable

## 摘要
建立儲存空間表。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 說明
**新的-AzureStorageTable** Cmdlet 會建立與 Azure 中的儲存空間帳戶相關聯的儲存空間表。

## 示例

### 範例1：建立 azure 儲存空間資料表
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

這個命令會建立名稱為 tableabc 的儲存空間資料表。

### 範例2：建立多個 azure 儲存空間資料表
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

這個命令會建立多個資料表。
它會使用 .NET **字串** 類別的 **Split** 方法，然後傳送管線上的名稱。

## 參數

### -內容
指定儲存內容。
若要建立它，您可以使用 New-AzureStorageContext Cmdlet。

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -名稱
指定新資料表的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### IStorageCoNtext

參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值

### 字串

形參 "Name" 接受管線中類型 "String" 的值

## 輸出

### AzureStorageTable WindowsAzure. ResourceModel。

## 筆記

## 相關連結

[AzureStorageTable](./Get-AzureStorageTable.md)

[移除-AzureStorageTable](./Remove-AzureStorageTable.md)


