---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f1575de761180c6ce17bcd6af1186d3e5bff60ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793237"
---
# Remove-AzTrafficManagerCustomHeaderFromEndpoint

## 摘要
從本機流量管理器端點物件移除自訂標頭資訊。

## 句法

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzTrafficManagerCustomHeaderFromEndpoint** Cmdlet 會從本機 Azure 流量管理器端點物件中移除自訂標頭資訊。
您可以使用 New-AzTrafficManagerEndpoint 或 Get-AzTrafficManagerEndpoint Cmdlet 來取得端點。

這個 Cmdlet 作用於本機端點物件。
使用 Set-AzTrafficManagerEndpoint Cmdlet，將您的變更提交至流量管理器的端點。

## 示例

### 範例1：從端點中移除自訂子網資訊
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

第一個命令會從名為 ResourceGroup11 的資源群組中，從名為 contoso 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。
第二個命令會從儲存在 $TrafficManagerEndpoint 中的端點中移除自訂標頭資訊。
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
指定要移除的自訂標頭資訊的名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerEndpoint 中的 TrafficManager。

## 輸出

### TrafficManagerEndpoint 中的 TrafficManager。

## 筆記

## 相關連結

[附加 AzTrafficManagerCustomHeaderToEndpoint](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerEndpoint.md)

[新-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerEndpoint](./Set-AzTrafficManagerEndpoint.md)
