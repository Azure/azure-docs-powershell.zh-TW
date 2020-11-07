---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967538"
---
# Remove-AzureTrafficManagerEndpoint

## 摘要
從流量管理器設定檔移除端點。

## 句法

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureTrafficManagerEndpoint** Cmdlet 會從 Microsoft Azure 流量管理器設定檔中移除端點。
移除端點之後，使用管線運算子將結果傳遞給 **AzureTrafficManagerProfile** Cmdlet。
該 Cmdlet 會連線至 Azure 以儲存您的變更。

## 示例

### 範例1：從設定檔移除端點
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

第一個命令使用 **AzureTrafficManagerProfile** Cmdlet 來取得名為 ContosoProfile 的設定檔，然後將它儲存在 $TrafficManagerProfile 變數中。

第二個命令會從 $TrafficManagerProfile 中儲存的流量管理器設定檔，移除具有 domain name Contoso02App.cloudapp.net 的端點。
命令會將設定檔物件傳遞給 **AzureTrafficManagerProfile** Cmdlet 以連線至 Azure，以儲存您的變更。

## 參數

### -功能變數名稱
指定要移除之端點的功能變數名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
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

### -TrafficManagerProfile
指定要從中移除端點的流量管理員設定檔物件。

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### TrafficManager. IProfileWithDefinition （WindowsAzure）
這個 Cmdlet 會產生流量管理器設定檔物件，其中包含已更新設定檔的相關資訊。

## 筆記

## 相關連結

[附加 AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


