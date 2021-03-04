---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910834"
---
# Set-AzTrafficManagerEndpoint

## 簡介
更新流量管理員端點。

## 語法

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-AzTrafficManagerEndpoint** Cmdlet 會更新 Azure 流量管理員中的端點。
此 Cmdlet 會更新來自本地端點物件的設定。
您可以使用 *TrafficManagerEndpoint* 參數或管道來指定端點物件。

您可以使用 Cmdlet 取得代表端點的Get-AzTrafficManagerEndpoint物件。
在本地修改物件，然後使用 **Set-AzTrafficManagerEndpoint** 來提交變更。

## 例子

### 範例 1：更新端點
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

第一個命令會使用 **Get-AzTrafficManagerEndpoint** Cmdlet 取得 Azure 流量管理員端點。
該命令將端點儲存在 $TrafficManagerEndpoint 變數中。

第二個命令會變更本地端點。
此命令將端點粗細變更為 20。

第三個命令會更新 Traffic Manager 中的端點，以符合 $TrafficManagerEndpoint。

## 參數

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

### -TrafficManagerEndpoint
指定一個本地 **TrafficManagerEndpoint** 物件。
此 Cmdlet 會更新流量管理員，以符合此本機物件。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint

## 輸出

### Microsoft.Azure.Commands.TrafficManager.models.TrafficManagerEndpoint

## 筆記

## 相關連結
