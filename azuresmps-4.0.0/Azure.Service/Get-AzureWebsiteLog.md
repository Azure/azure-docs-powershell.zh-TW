---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967952"
---
# Get-AzureWebsiteLog

## 摘要
取得指定網站的記錄。

## 句法

### 側
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

取得指定網站的記錄。

## 示例

### 範例1：開始記錄串流
```
PS C:\> Get-AzureWebsiteLog -Tail
```

這個範例會啟動所有應用程式記錄的記錄傳送。

### 範例2：開始記錄 HTTP 記錄的資料流程
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

這個範例會啟動 HTTP 記錄的記錄傳送。

### 範例3：開始記錄資料流程以尋找錯誤記錄
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

這個範例會開始記錄資料流程並只顯示錯誤記錄。

### 範例4：顯示 avaiable 記錄
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

這個範例會列出網站中所有可用的記錄路徑。

## 參數

### -ListPath
指出是否要列出記錄路徑。

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -訊息
指定將用來篩選記錄訊息的字串。
只會檢索包含此字串的記錄。

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
網站的名稱。

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

### -Path
要從哪個路徑檢索記錄。
根據預設，它是 Root，也就是包含所有路徑。

```yaml
Type: String
Parameter Sets: Tail
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
指定槽名稱。

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

### -尾
指定是否要資料流記錄。

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
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

[新-AzureWebsite](./New-AzureWebsite.md)

[移除-AzureWebsite](./Remove-AzureWebsite.md)

[開始-AzureWebsite](./Start-AzureWebsite.md)


