---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445275"
---
# Get-AzureStorageTable

## 摘要
列出儲存資料表。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### TableName (預設) 
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 說明
**AzureStorageTable** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間資料表。

## 示例

### 範例1：列出所有 Azure 儲存空間資料表
```
PS C:\>Get-AzureStorageTable
```

這個命令會取得儲存空間帳戶的所有儲存空間資料表。

### 範例2：使用萬用字元列出 Azure 儲存空間資料表
```
PS C:\>Get-AzureStorageTable -Name table*
```

這個命令使用萬用字元來取得名稱以 table 開頭的儲存資料表。

### 範例3：使用表格名稱首碼列出 Azure 儲存空間資料表
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

這個命令會使用 *Prefix* 參數來取得名稱以 table 開頭的儲存空間資料表。

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
指定資料表名稱。
如果資料表名稱是空值，該 Cmdlet 會列出所有的資料表。
否則，它會列出符合指定名稱或一般名稱模式的所有資料表。

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### -Prefix
指定要取得的資料表名稱中所用的首碼。
您可以使用此程式來找出所有以相同字串（例如 table）開頭的資料表。

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

[新-AzureStorageTable](./New-AzureStorageTable.md)

[移除-AzureStorageTable](./Remove-AzureStorageTable.md)


