---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6d9ec806c1456f572991f7c72189c47abbe9ffe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910850"
---
# New-AzTrafficManagerEndpoint

## 簡介
在流量管理員設定檔中建立端點。

## 語法

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzTrafficManagerEndpoint** Cmdlet 在 Azure 流量管理員設定檔中建立端點。

此 Cmdlet 會向流量管理員服務提交每個新端點。
若要在單一作業中新增多個端點至本地流量管理員設定檔物件並提交變更，請使用 Add-AzTrafficManagerEndpointConfig Cmdlet。

## 例子

### 範例 1：建立設定檔的外部端點
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

此命令在資源群組中名為 ContosoProfile 的設定檔中，建立名為 contoso 的外部端點，名為 ResourceGroup11。

### 範例 2：建立設定檔的 Azure 端點
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

此命令在資源群組 ResourceGroup11 中名為 ContosoProfile 的設定檔中，建立名為 contoso 的 Azure 端點。
Azure 端點指向 Azure Web App，其 Azure Resource Manager 識別碼是由 *TargetResourceId* 中的 URI 路徑所提供。
此命令不會指定 *端點位置* 參數，因為 Web App 資源會提供位置。

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
使用'地理'流量路由方法時對應到此端點的區域清單。 如需接受值的完整清單，請參閱流量管理員檔。

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
指定 Azure 地區名稱。
有關 Azure 區域的完整清單，請參閱 Azure 區域 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) (。

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

### -名稱
指定此 Cmdlet 所建立的流量管理員端點名稱。

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

### -ProfileName
指定此 Cmdlet 新增端點的流量管理員設定檔名稱。
若要取得設定檔，請使用New-AzTrafficManagerProfile或Get-AzTrafficManagerProfile Cmdlet。

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

### -ResourceGroupName
指定資源組的名稱。
此 Cmdlet 會在此參數指定的群組中建立流量管理員端點。

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

### -類型
指定此 Cmdlet 新增到流量管理員設定檔的端點類型。
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

### 沒有

## 輸出

### Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint

## 筆記

## 相關連結

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


