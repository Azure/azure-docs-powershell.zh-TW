---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127965"
---
# Add-AzTrafficManagerCustomHeaderToEndpoint

## 摘要
將自訂標頭資訊新增到本機流量管理器端點物件。

## 句法

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**載入 AzTrafficManagerCustomHeaderToEndpoint** Cmdlet 會將自訂標頭資訊新增到本機 Azure 流量管理器端點物件。
您可以使用 New-AzTrafficManagerEndpoint 或 Get-AzTrafficManagerEndpoint Cmdlet 來取得端點。

這個 Cmdlet 作用於本機端點物件。
使用 Set-AzTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。

## 示例

### 範例1：將自訂標頭資訊新增到端點
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

第一個命令會使用 **AzTrafficManagerEndpoint** Cmdlet 來建立 Azure 流量管理器端點。
該命令會將本機端點儲存在 $TrafficManagerEndpoint 變數中。
第二個命令會將自訂標頭資訊新增至儲存在 $TrafficManagerEndpoint 中的端點。
Final 命令會更新流量管理器中的端點，以符合 $TrafficManagerEndpoint 中的本機值。

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
指定要新增之自訂標頭資訊的名稱。

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

### -TrafficManagerEndpoint
指定本機 **TrafficManagerEndpoint** 物件。
這個 Cmdlet 會修改這個本機物件。
若要取得 **TrafficManagerEndpoint** 物件，請使用 Get-AzTrafficManagerEndpoint 或 New-AzTrafficManagerEndpoint Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -值
指定要新增之自訂標頭資訊的值。

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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
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

### TrafficManagerEndpoint 中的 TrafficManager。

## 筆記

## 相關連結

[移除-AzTrafficManagerCustomHeaderFromEndpoint](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[新-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
