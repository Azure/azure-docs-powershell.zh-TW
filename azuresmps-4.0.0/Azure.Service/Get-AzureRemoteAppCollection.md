---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8F00099A-042A-4450-B6CF-9EDA2350CBFC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94e1711bc42745b872a8e2abc8cf82e5e0e67db9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967775"
---
# Get-AzureRemoteAppCollection

## 摘要
檢索 Azure RemoteApp 集合的相關資訊。

## 句法

```
Get-AzureRemoteAppCollection [[-CollectionName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureRemoteAppCollection** Cmdlet 會在 Microsoft Azure 中檢索 Azure RemoteApp 集合的相關資訊。
它會傳回包含特定集合之資訊的物件，或者如果沒有指定集合，則會傳回目前訂閱中所有集合的相關資訊。

## 示例

### 範例1：取得所有集合的清單
```
PS C:\> Get-AzureRemoteAppCollection
```

這個命令會傳回訂閱中所有 Azure RemoteApp 集合的清單。

### 範例2：取得指定集合的相關資訊
```
PS C:\> Get-AzureRemoteAppCollection ContosoApps
```

這個命令會傳回名為 ContosoApps 的 Azure RemoteApp 集合的相關資訊。

### 範例3：使用萬用字元取得收藏清單
```
PS C:\> Get-AzureRemoteAppCollection Finance*
```

這個命令會傳回符合金融的所有 Azure RemoteApp 集合的清單 *。

## 參數

### -CollectionName
指定 Azure RemoteApp 集合的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[新-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[移除-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[更新-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


