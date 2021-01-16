---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280119"
---
# Get-AzStorageTable

## 摘要
列出儲存資料表。

## 句法

### TableName (預設) 
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TablePrefix
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzStorageTable** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間資料表。

## 示例

### 範例1：列出所有 Azure 儲存空間資料表
```
PS C:\>Get-AzStorageTable
```

這個命令會取得儲存空間帳戶的所有儲存空間資料表。

### 範例2：使用萬用字元列出 Azure 儲存空間資料表
```
PS C:\>Get-AzStorageTable -Name table*
```

這個命令使用萬用字元來取得名稱以 table 開頭的儲存資料表。

### 範例3：使用表格名稱首碼列出 Azure 儲存空間資料表
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

這個命令會使用 *Prefix* 參數來取得名稱以 table 開頭的儲存空間資料表。

## 參數

### -內容
指定儲存內容。
若要建立它，您可以使用 New-AzStorageContext Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定資料表名稱。
如果資料表名稱是空值，該 Cmdlet 會列出所有的資料表。
否則，它會列出符合指定名稱或一般名稱模式的所有資料表。

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
指定要取得的資料表名稱中所用的首碼。
您可以使用此程式來找出所有以相同字串（例如 table）開頭的資料表。

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### IStorageCoNtext 中的 [Common.]

## 輸出

### AzureStorageTable WindowsAzure. ResourceModel。

## 筆記

## 相關連結

[新-AzStorageTable](./New-AzStorageTable.md)

[移除-AzStorageTable](./Remove-AzStorageTable.md)


