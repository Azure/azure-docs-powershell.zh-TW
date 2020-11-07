---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966880"
---
# Set-AzureTrafficManagerEndpoint

## 摘要
更新流量管理器設定檔中端點的屬性。

## 句法

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureTrafficManagerEndpoint** Cmdlet 會更新 Microsoft Azure 流量管理器設定檔中端點的屬性。
如果端點在目前的設定檔中不存在，此 Cmdlet 會建立它。
在您新增端點之後，使用管線運算子將結果傳遞給 **AzureTrafficManagerProfile** Cmdlet。
該 Cmdlet 會連線至 Azure 以儲存您的變更。

## 示例

### 範例1：更新設定檔的端點
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

第一個命令使用 **AzureTrafficManagerProfile** Cmdlet 來取得名為 ContosoProfile 的設定檔，然後將它儲存在 $TrafficManagerProfile 變數中。

第二個命令會更新 $TrafficManagerProfile 中儲存的流量管理器設定檔中的端點。
端點會有 [功能變數名稱 ContosoApp02.cloudapp.net]。
該命令也會指定端點的狀態、類型、粗細和位置。
該命令會將修改過的設定檔傳遞給 **AzureTrafficManagerProfile** Cmdlet，以連線至 Azure 以儲存您的變更。

## 參數

### -功能變數名稱
指定要修改之端點的功能變數名稱。

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

### -位置
指定 Cmdlet 所新增之端點的位置。
這必須是 Azure 位置。

此參數必須在已將負載平衡方法設定為 "效能" 的設定檔中，包含類型 "Any" 或 "TrafficManager" 類型的端點的值。
可能的值是 Azure 地區名稱，如所列  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ 。

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

### -MinChildEndpoints
指定嵌套設定檔必須以線上方式將此端點視為線上的最小端點數。

```yaml
Type: Int32
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

### -狀態
指定監視端點的狀態。
有效值為： 

- 後
- 禁止

如果您指定的值為 [已啟用]，流量管理器會監視端點，且負載平衡方法會在管理流量時考慮它。

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

### -TrafficManagerProfile
指定要為其修改端點的流量管理器設定檔物件。

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

### -類型
指定端點的類型。
有效值為： 

- CloudService
- AzureWebsite
- TrafficManager

- 每 

如果有一個以上的 AzureWebsite 端點，端點必須位於不同的資料中心。

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

### 寬度
指定 Cmdlet 所新增之端點的權重。
這個參數的有效值範圍是 \[ 1，1000 \] 。

這個參數只適用于 RoundRobin 負載平衡原則。

```yaml
Type: Int32
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
這個 Cmdlet 會產生流量管理器設定檔物件，其中包含已更新設定檔的相關資訊。

## 筆記

## 相關連結

[附加 AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[移除-AzureTrafficManagerEndpoint](./Remove-AzureTrafficManagerEndpoint.md)

[AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


