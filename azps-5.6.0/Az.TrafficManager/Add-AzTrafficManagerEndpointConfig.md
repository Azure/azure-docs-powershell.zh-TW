---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910877"
---
# Add-AzTrafficManagerEndpointConfig

## 簡介
新增端點至本地流量管理員設定檔物件。

## 語法

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-AzTrafficManagerEndpointConfig** Cmdlet 會新增端點至本地 Azure 流量管理員設定檔物件。
您可以使用 Cmdlet 或 Cmdlet New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile設定檔。

此 Cmdlet 可在本地設定檔物件上操作。
使用 Cmdlet 來針對流量管理員的設定檔Set-AzTrafficManagerProfile變更。
若要在單一作業中建立端點並提交變更，請使用 New-AzTrafficManagerEndpoint Cmdlet。

## 例子

### 範例 1：新增端點至設定檔
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

第一個命令會使用 **Get-AzTrafficManagerProfile** Cmdlet 取得 Azure 流量管理員設定檔。
該命令將本地設定檔儲存在 $TrafficManagerProfile 變數中。

第二個命令會將名為 contoso 的端點新增到儲存在 $TrafficManagerProfile。
該命令包含端點的群組原則資料。
此命令只會變更本機物件。

最後一個命令會更新 Azure 中的流量管理員設定檔，以與 $TrafficManagerProfile。

## 參數

### -CustomHeader
建議要求之自訂標題名稱和值組清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
指定要用於 Performance 流量路由方法的端點位置。
此參數僅適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。
使用 Performance 流量路由方法時，您必須指定此參數。

指定 Azure 地區名稱。
有關 Azure 區域的完整清單，請參閱 Azure 區域 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
指定此 Cmdlet 新增的流量管理員端點名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointStatus
指定端點的狀態。
有效的值為： 

- 啟用 
- 禁用 

如果狀態為 Enabled，端點會針對端點健康情況進行安排，並包含在流量路由方法中。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeoMapping
使用'地理'流量路由方法時對應到此端點的區域清單。 如需接受值的完整清單，請參閱流量管理員 [檔](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)。

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinChildEndpoints
若要將父設定檔中的巢式端點視為可用，子設定檔中必須有的端點數目為最小值。
僅適用于類型為 "NestedEndpoints" 的端點。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -優先順序
指定流量管理員指派給端點的優先順序。
只有在流量管理員設定檔設定為優先順序流量路由方法時，才能使用此參數。
有效值是 1 到 1000 的整數。
較低值代表較高的優先順序。

如果您指定優先順序，則必須指定設定檔中所有端點的優先順序，而且沒有兩個端點可以共用相同的優先順序值。
如果您未指定優先順序，流量管理員會以設定檔列出端點的順序，為端點指派預設優先順序值，從 (1) 開始。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -子網映射
使用子網流量路由方法時，對應到此端點的位址範圍或子網清單。

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -目標
指定端點的完全 DNS 名稱。
流量管理員在將流量引導至此端點時，會于 DNS 回應中回回此值。
僅針對 ExternalEndpoints 端點類型指定此參數。
針對其他端點類型，請改為指定 *TargetResourceId* 參數。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceId
指定目標的資源識別碼。
僅針對 AzureEndpoints 和 NestedEndpoints 端點類型指定此參數。
針對 ExternalEndpoints 端點類型，請改為指定 *Target* 參數。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
指定一個本地 **TrafficManagerProfile** 物件。
此 Cmdlet 會修改此本機物件。
若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -類型
指定此 Cmdlet 新增到 Azure 流量管理員設定檔的端點類型。
有效的值為： 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -重量
指定流量管理員指派給端點的粗細。
有效值是 1 到 1000 的整數。
預設值為 1 (1) 。
只有在使用加權流量路由方法設定流量管理員設定檔時，才能使用此參數。

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile

## 輸出

### Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerProfile

## 筆記

## 相關連結

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


