---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 6477a9f8c3830fa8ca8a74780db560455eb61dfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450628"
---
# Get-AzureRmDataLakeStoreChildItem

## 摘要
取得 Data Lake Store 中資料夾中的專案清單。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmDataLakeStoreChildItem** Cmdlet 會取得 Data Lake store 中資料夾中的專案清單。

## 示例

### 範例1：取得資料夾的子專案
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

這個命令會取得 MyFiles 資料夾的子專案。

## 參數

### -帳戶
指定 Data Lake Store 帳戶的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定資料夾的 Data Lake Store 路徑，從 root 目錄開始 (/) 。

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### IEnumerable<DataLakeStoreItem>
在指定路徑下的 Data Lake Store 檔案和資料夾清單。

## 筆記

## 相關連結

