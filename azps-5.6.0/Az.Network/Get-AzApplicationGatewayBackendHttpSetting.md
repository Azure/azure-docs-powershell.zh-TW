---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 957417d7751080a82ddc8785abdd124c8f723303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915357"
---
# Get-AzApplicationGatewayBackendHttpSetting

## 簡介
獲得應用程式閘道的後端 HTTP 設定。

## 語法

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
Cmdlet Get-AzApplicationGatewayBackendHttpSetting Cmdlet 會獲得應用程式閘道的後端 HTTP 設定。

## 例子

### 範例 1：按名稱取得後端 HTTP 設定
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會獲得名稱為 Settings01 的 HTTP 設定$AppGw將設定儲存在$Settings變數中。

### 範例 2：取得後端 HTTP 設定的集合
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會收集您$AppGw HTTP 設定，並儲存在$SettingsList變數中。

## 參數

### -ApplicationGateway
指定包含後端 HTTP 設定的應用程式閘道物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -名稱
指定此 Cmdlet 所獲得後端 HTTP 設定的名稱。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Network.models.PSApplicationGateway

## 輸出

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings

## 筆記

## 相關連結

[Add-AzApplicationGatewayBackendHttpSetting](./Add-AzApplicationGatewayBackendHttpSetting.md)

[New-AzApplicationGatewayBackendHttpSetting](./New-AzApplicationGatewayBackendHttpSetting.md)

[Remove-AzApplicationGatewayBackendHttpSetting](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[Set-AzApplicationGatewayBackendHttpSetting](./Set-AzApplicationGatewayBackendHttpSetting.md)

