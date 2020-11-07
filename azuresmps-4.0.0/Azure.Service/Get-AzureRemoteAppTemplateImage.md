---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968025"
---
# Get-AzureRemoteAppTemplateImage

## 摘要
檢索 Azure RemoteApp 範本影像的相關資訊。

## 句法

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureRemoteAppTemplateImage** Cmdlet 會在 Microsoft Azure 中檢索 Azure RemoteApp 範本影像的相關資訊。
這個 Cmdlet 會傳回包含指定範本影像相關資訊的物件。
如果未指定任何範本圖像，則會檢索目前訂閱中所有範本影像的相關資訊。

## 示例

### 範例1：取得所有範本影像的清單
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

這個命令會傳回所有範本影像的清單。

### 範例2：檢索指定範本圖像的相關資訊
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

這個命令會檢索名為 ContosoApps 的範本影像的相關資訊。

## 參數

### -ImageName
指定 Azure RemoteApp 範本影像的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

[AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[AzureRemoteAppStartMenuProgram](./Get-AzureRemoteAppStartMenuProgram.md)


