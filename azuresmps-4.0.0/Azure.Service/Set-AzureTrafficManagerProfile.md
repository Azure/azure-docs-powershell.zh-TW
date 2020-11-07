---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967240"
---
# Set-AzureTrafficManagerProfile

## 摘要
更新流量管理器設定檔的屬性。

## 句法

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureTrafficManagerProfile** Cmdlet 會更新 Microsoft Azure 流量管理器設定檔的屬性。

針對您已將 *LoadBalancingMethod* 值設定為「容錯移轉」的設定檔，您可以使用 Add-AzureTrafficManagerEndpoint Cmdlet 來判斷您已新增至設定檔的端點的容錯移轉順序。
如需詳細資訊，請參閱下方的範例3。

## 示例

### 範例1：設定流量管理器設定檔的 TTL
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

這個命令會將流量管理器設定檔物件 MyTrafficManagerProfile 的 TTL 設定為60秒。

### 範例2：設定多個設定檔的值
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

這個命令會使用 **AzureTrafficManagerProfile** Cmdlet 取得名為 MyProfile 的流量管理器設定檔。
設定檔會使用 RoundRobin 負載平衡方法、30秒的 TTL、監視器通訊協定 HTTP、監視器埠，以及流量管理器設定檔的相對路徑。

### 範例3：將端點重新排序至所需的容錯移轉順序
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

這個範例會將新增至 MyProfile 的端點重新排序為想要的容錯移轉順序。

第一個命令會取得名為 MyProfile 的流量管理器設定檔物件，並將物件儲存在 $Profile 變數中。

第二個命令會將端點陣列中的端點重新排序為應發生容錯移轉的順序。

最後一個命令會使用新的端點順序，更新 $Profile 中儲存的流量管理器設定檔。

## 參數

### -LoadBalancingMethod
指定用來散佈連接的負載平衡方法。
有效值為： 

- 提高
- 實現
- RoundRobin

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

### -MonitorPort
指定用來監視端點健康情況的埠。
有效值為大於0且小於或等於65535的整數值。

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

### -MonitorProtocol
指定用來監視端點健康情況的通訊協定。
有效值為： 

- Http
- Ip-HTTPs

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

### -MonitorRelativePath
指定要探測健康狀態的端點網功能變數名稱稱相對路徑。
路徑必須符合下列限制： 

- 路徑必須是1到1000個字元。
- 它必須以正斜線（/）開頭。
- 它不能包含 XML 元素 \<\> 。
- 它必須不包含雙斜杠（//）。
- 它必須包含不正確 HTML 逸出字元。
例如，% XY。

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

### -名稱
指定要更新的流量管理器設定檔名稱。

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
指定您用來設定設定檔的流量管理器設定檔物件。

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

### -Ttl
指定 DNS 存留時間 (TTL) ，該 TTL 會通知當地的 DNS 解析程式緩存 DNS 專案的時間長度。
有效值為30到999999的整數。

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
這個 Cmdlet 會產生流量管理器設定檔物件。

## 筆記

## 相關連結

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[新-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[移除-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)


