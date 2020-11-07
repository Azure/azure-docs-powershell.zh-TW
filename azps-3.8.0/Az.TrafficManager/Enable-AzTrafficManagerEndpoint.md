---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957583"
---
# Enable-AzTrafficManagerEndpoint

## 摘要
啟用流量管理器設定檔中的端點。

## 句法

### 區域
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 面向
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Enable-AzTrafficManagerEndpoint** Cmdlet 可在 Azure 流量管理器設定檔中啟用端點。

您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數來指定 **TrafficManagerEndpoint** 物件。

或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。

## 示例

### 範例1：從設定檔啟用端點
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

這個命令會在 [資源群組 ResourceGroup11] 中，將名為 ContosoProfile 的設定檔中的外部端點啟用為 contoso。

### 範例2：使用管線啟用端點
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。
然後，命令會使用管線運算子將該端點傳遞到 **Enable AzTrafficManagerEndpoint** Cmdlet。
該 Cmdlet 可啟用該端點。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -名稱
指定此 Cmdlet 啟用之流量管理器端點的名稱。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
指定此 Cmdlet 啟用端點的流量管理器設定檔名稱。
若要取得設定檔，請使用 Get-AzTrafficManagerProfile Cmdlet。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。
這個 Cmdlet 可在此參數指定的群組中啟用流量管理器端點。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
指定此 Cmdlet 啟用的流量管理器端點。
若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -類型
指定此 Cmdlet 在流量管理器設定檔中停用的端點類型。
有效值為： 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerEndpoint 中的 TrafficManager。

## 輸出

### System.object

## 筆記

## 相關連結

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[新-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[新-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[移除-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


