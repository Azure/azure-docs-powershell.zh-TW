---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967265"
---
# Set-AzureServiceProject

## 摘要
為目前的服務設定預設位置、訂閱、槽及儲存空間帳戶。

## 句法

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureServiceProject** Cmdlet 會設定目前服務的部署位置、槽、儲存空間帳戶及訂閱。
每當服務發佈到雲端時，就會使用這些值。

## 示例

### 範例1：基本設定
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

將服務的部署位置設定為北中美區域。
將部署槽位設定為 [生產]。 設定將用來將服務定義暫存至 myStorageAccount 的儲存空間帳戶。
設定將託管服務的訂閱進行 mySubscription。
每當服務發佈到雲端時，系統會將它託管在資料中心的 [北部] 美國地區，它會更新部署槽，而且會使用指定的訂閱和儲存空間帳戶。

## 參數

### -位置
將託管服務的地區。
每當服務發佈到雲端時，就會使用這個值。
可能的值包括：亞洲、歐洲、美國、東亞、東、北部、北部、北美、美國、東南部、西歐、華南、東南部、西亞、西美、北美國、西歐、美國等。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
表示此 Cmdlet 會傳回代表其操作專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -槽
要託管服務的槽 (生產或暫存) 。
每當服務發佈到雲端時，就會使用這個值。
可能的值包括：生產、分段。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 儲存空間
將服務套件上傳到雲端時要使用的儲存空間帳戶。
如果儲存帳戶不存在，則會在服務發佈到雲端時建立。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記
* 節點開發人員、php 開發人員、python-開發人員

## 相關連結

[新-AzureServiceProject](./New-AzureServiceProject.md)

[發佈-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


