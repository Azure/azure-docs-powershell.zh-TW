---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966982"
---
# Get-AzureTrafficManagerProfile

## 摘要
取得流量管理器設定檔的詳細資料。

## 句法

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureTrafficManagerProfile** Cmdlet 會取得 Microsoft Azure 流量管理器設定檔的詳細資料。
如果您沒有指定 *Name* 參數，此 Cmdlet 會列出目前訂閱中的流量管理器設定檔。

## 示例

### 範例1：取得訂閱中流量管理器設定檔的清單
```
PS C:\>Get-AzureTrafficManagerProfile
```

這個命令會在您的訂閱中取得流量管理器配置檔案清單。

### 範例2：取得流量管理器設定檔
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

這個命令會取得名為 MyProfile 的流量管理器設定檔。

### 範例3：將端點新增至流量管理器設定檔
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

這個命令會將端點新增到流量管理器設定檔，然後儲存設定檔。

## 參數

### -名稱
指定要取得的流量管理器設定檔名稱。

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

## 輸出

### TrafficManager. IProfileWithDefinition （WindowsAzure）
這個 Cmdlet 會產生流量管理器設定檔物件或物件。

## 筆記

## 相關連結

[附加 AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[新-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[移除-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


