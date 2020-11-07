---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: ed3468e6064aa28595ddbcb5f4c296976dd5fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793239"
---
# Disable-AzTrafficManagerEndpoint

## 摘要
停用流量管理器設定檔中的端點。

## 句法

### 區域
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### 面向
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**Disable AzTrafficManagerEndpoint** Cmdlet 會停用 Azure 流量管理器設定檔中的端點。

您可以使用管線運算子，將 **TrafficManagerEndpoint** 物件傳遞到這個 Cmdlet，或者您可以使用 *TrafficManagerEndpoint* 參數傳遞 **TrafficManagerEndpoint** 物件。

或者，您也可以使用 *name* 和 *type* 參數來指定端點名稱和類型，以及 *ProfileName* 和 *ResourceGroupName* 參數。

## 示例

### 範例1：依名稱停用端點
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

這個命令會停用 [資源群組 ResourceGroup11] 中名為 ContosoProfile 的設定檔中名為 [contoso] 的外部端點。
命令會提示您進行確認。

### 範例2：使用管線停用端點
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

這個命令會從 ResourceGroup11 中名為 ContosoProfile 的設定檔中取得名為 Contoso 的外部端點。
然後，命令會使用管線運算子將該端點傳遞到 **Disable AzTrafficManagerEndpoint** Cmdlet。
該 Cmdlet 會停用該端點。
命令會指定 *Force* 參數。
因此，它不會提示您進行確認。

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

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 停用之流量管理器端點的名稱。

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
指定此 Cmdlet 停用端點的流量管理器設定檔名稱。
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
這個 Cmdlet 會停用此參數指定之群組中的流量管理器端點。

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
指定此 Cmdlet 停用的流量管理器端點。
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
指定此 Cmdlet 新增至流量管理器設定檔的端點類型。
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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerEndpoint 中的 TrafficManager。

## 輸出

### System.object

## 筆記

## 相關連結

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[新-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[新-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[移除-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


