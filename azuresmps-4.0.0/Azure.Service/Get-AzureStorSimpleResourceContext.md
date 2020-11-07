---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967995"
---
# Get-AzureStorSimpleResourceContext

## 摘要
取得目前的資源內容。

## 句法

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleResourceCoNtext** Cmdlet 會取得目前的資源內容。

## 示例

### 範例1：取得目前的內容
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

第一個命令會使用 **AzureStorSimpleResource** Cmdlet，將目前的內容設為名為 Contoso63-Tsqa 的資源。

第二個命令會取得目前的資源內容。

### 範例2：嘗試取得目前的內容
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

這個命令會取得目前的內容。
在這個範例中，沒有設定任何內容。
命令會傳回說明問題的訊息。

## 參數

### -設定檔
指定 Azure 設定檔。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### StorSimpleResourceCoNtext
這個 Cmdlet 會傳回 **ResourceCoNtext** 物件。

## 筆記

## 相關連結

[AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[選取-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


