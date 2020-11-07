---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967122"
---
# Get-AzureAccount

## 摘要
取得可供 Azure PowerShell 使用的 Azure 帳戶。

## 句法

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureAccount** Cmdlet 會取得適用于 Windows PowerShell 的 Azure 帳戶。
若要讓您的帳戶可供 Windows PowerShell 使用，請使用 **AzureAccount** 或 **Import PublishSettingsFile** Cmdlet。

## 示例

### 範例1：取得所有帳戶
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

這個命令會取得與指定使用者相關聯的所有帳戶。

### 範例2：依名稱取得帳戶
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

這個命令會取得 ContosoAdmin 帳戶。

## 參數

### -名稱
只取得指定的帳號。
預設值為所有可供 Windows PowerShell 使用的帳戶。
輸入帳戶名稱。
[ **名稱** ] 值會區分大小寫。
不允許使用萬用字元。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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
您無法將輸入管到這個 Cmdlet。

## 輸出

### 所有
這個 Cmdlet 不會傳回任何輸出。

## 筆記

## 相關連結

[附加 AzureAccount](./Add-AzureAccount.md)

[AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[匯入-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[移除-AzureAccount](./Remove-AzureAccount.md)


