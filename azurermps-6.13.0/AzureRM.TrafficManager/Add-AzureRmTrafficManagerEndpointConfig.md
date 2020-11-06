---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3c77ca67999ffa9cecbe35de4d4533f5d163f17f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455887"
---
# Add-AzureRmTrafficManagerEndpointConfig

## 摘要
將端點新增到本機流量管理器設定檔物件。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmTrafficManagerEndpointConfig** Cmdlet 會將端點新增到本機 Azure 流量管理器設定檔物件。
您可以使用 New-AzureRmTrafficManagerProfile 或 Get-AzureRmTrafficManagerProfile Cmdlet 來取得設定檔。

這個 Cmdlet 作用於本機設定檔物件。
使用 Set-AzureRmTrafficManagerProfile Cmdlet，將您的變更提交至流量管理器的設定檔。
若要建立端點並在單一作業中提交變更，請使用 New-AzureRmTrafficManagerEndpoint Cmdlet。

## 示例

### 範例1：在設定檔中新增端點
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

第一個命令會使用 **AzureRmTrafficManagerProfile** Cmdlet 取得 Azure 流量管理器設定檔。
該命令會將本機設定檔儲存在 $TrafficManagerProfile 變數中。

第二個命令會將名為 contoso 的端點新增至儲存在 $TrafficManagerProfile 中的設定檔。
此命令包含端點的配置資料。
這個命令只會變更本機物件。

Final 命令會更新 Azure 中的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。

## 參數

### -CustomHeader
針對探測要求的自訂標頭名稱和值對清單。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointLocation
指定要在效能流量路由方法中使用的端點位置。
這個參數只適用于 ExternalEndpoints 或 NestedEndpoints 類型的端點。
使用效能流量路由方法時，您必須指定此參數。

指定 Azure 地區名稱。
如需 Azure 區域的完整清單，請參閱 Azure 地區 https://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/) 。

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

### -終結點
指定此 Cmdlet 所新增之流量管理器端點的名稱。

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
有效值為： 

- 後 
- 禁止 

如果狀態為 [已啟用]，則會針對端點健康情況探測端點，並包含在流量路由方法中。

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
使用 ' 地理 ' 流量路由方法時，對應到此端點的地區清單。 如需可 [接受值的完整清單](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)，請參閱流量管理器檔。

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
必須在子設定檔中提供的端點的最小數目，才能認為父設定檔中的嵌套端點可供使用。
僅適用于類型 ' NestedEndpoints」的端點。

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
指定流量管理器指派給端點的優先順序。
只有在流量管理器設定檔是以優先順序流量路由方法設定的情況下，才能使用這個參數。
有效的值是從1到1000的整數。
較低的值代表較高的優先順序。

如果您指定優先順序，您必須在設定檔中的所有端點上指定優先順序，而且任何兩個端點都不能共用相同的優先順序值。
如果您沒有指定優先順序，流量主管會將預設的優先順序值指派給端點，並從一個 (1) 開始，並依照設定檔列出端點的順序進行。

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

### -SubnetMapping
使用 [™̃Subnetâ] 流量路由方法時，對應至此端點的位址範圍或子網清單。

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
指定端點的完整 DNS 名稱。
當流量主管將流量導向到此端點時，會在 DNS 回應中傳回這個值。
請僅針對 ExternalEndpoints 端點類型指定此參數。
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
針對 ExternalEndpoints 端點類型，請改為指定 *目標* 參數。

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
指定本機 **TrafficManagerProfile** 物件。
這個 Cmdlet 會修改這個本機物件。
若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。

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
指定此 Cmdlet 新增至 Azure 流量管理器設定檔的端點類型。
有效值為： 

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

### 寬度
指定流量主管指派給端點的權重。
有效的值是從1到1000的整數。
預設值是一個 (1) 。
只有在流量管理器設定檔是使用加權流量路由方法設定的情況下，才能使用這個參數。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerProfile （）
這個 Cmdlet 接受 **TrafficManagerProfile** 物件到這個 Cmdlet。

## 輸出

### TrafficManagerProfile （）
這個 Cmdlet 會傳回修改過的 **TrafficManagerProfile** 物件。

## 筆記

## 相關連結

[AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[新-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[移除-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


