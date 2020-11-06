---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457608"
---
# Set-AzureRmDataLakeStoreItemExpiry

## 摘要
針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzureRmDataLakeStoreItemExpiry** Cmdlet 會針對 Azure Data Lake store 帳戶中的檔案，設定或移除到期時間。

## 示例

### 範例1：設定檔案的到期時間
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

從現在開始，將 [帳戶 ContosoADL] 中的檔案 myfile.txt 為兩個小時。
這會造成檔案到期， (會在兩個小時內標示為刪除) 。

### 範例2：移除檔案的到期日
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

移除先前在帳戶 "ContosoADL" 中的檔案 ' myfile.txt ' 上設定的任何過期時間。
這表示檔案不會自動過期， (會將它標記為 [刪除]) 且必須手動刪除，或將它設為再次過期。

## 參數

### -帳戶
指定 Data Lake Store 帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -到期日
指定檔案的絕對到期時間。
如果沒有值或設定為 [無法]，檔案就不會過期。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
指定要設定或移除到期之檔專案的資料 Lake Store 路徑。

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### DataLakeStoreItem
已更新的檔案，包含新的到期時間。

## 筆記
別名： Set-AdlStoreItemExpiry

## 相關連結

[AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

