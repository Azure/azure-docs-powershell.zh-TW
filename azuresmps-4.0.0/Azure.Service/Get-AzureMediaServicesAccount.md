---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967781"
---
# Get-AzureMediaServicesAccount

## 摘要
取得可用的 Azure 媒體服務帳戶。

**注意：** 此版本已棄用，請參閱 [較新的版本](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)。

## 句法

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

若要列出所有帳戶，請使用 `Get-AzureMediaServicesAccount` Cmdlet。
若要取得特定帳戶的詳細資訊，請使用 `Get-AzureMediaServicesAccount -Name YourAccountName` Cmdlet。

## 示例

### 範例1：列出所有媒體服務帳戶
```
PS C:\> Get-AzureMediaServicesAccount
```

這個命令會列出所有可用的媒體服務帳戶。

### 範例2：取得媒體服務帳戶的詳細資訊
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

這個命令會顯示媒體服務帳戶的屬性。

## 參數

### -名稱
媒體服務帳戶名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[如何使用 Azure PowerShell for 媒體服務](https://go.microsoft.com/fwlink/?LinkId=324179)


