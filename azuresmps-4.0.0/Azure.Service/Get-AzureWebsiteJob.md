---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967719"
---
# Get-AzureWebsiteJob

## 摘要
取得與網站相關聯的 web 作業。

## 句法

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
取得與網站相關聯的 web 作業。

## 示例

### 範例1：取得特定的網頁作業資訊
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

從 MyWebsite 生產槽取得名為 MyWebJob 的 web 作業。

### 範例2：取得網站的所有網頁作業
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

取得與 MyWebsite 生產槽相關聯的所有 web 作業。

### 範例3：取得所有觸發的 web 作業
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

從 MyWebsite 的分段槽取得所有觸發的 web 作業。

## 參數

### -JobName
Web 作業名稱

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

### -JobType
Web 作業類型。
此參數可接受的值為：

- 引起
- 連續性

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

### -名稱
Azure 網站的名稱。

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
Azure 網站的槽名稱。

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

## 相關連結

[AzureWebsite](./Get-AzureWebsite.md)

[新-AzureWebsiteJob](./New-AzureWebsiteJob.md)

[移除-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[開始-AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[停止 AzureWebsiteJob](./Stop-AzureWebsiteJob.md)


