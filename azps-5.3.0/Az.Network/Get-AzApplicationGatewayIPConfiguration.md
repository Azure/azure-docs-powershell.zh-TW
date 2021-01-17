---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450231"
---
# Get-AzApplicationGatewayIPConfiguration

## 摘要
取得應用程式閘道的 IP 配置。

## 句法

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzApplicationGatewayIPConfiguration** Cmdlet 會取得應用程式閘道的 IP 配置。
[IP 設定] 包含部署應用程式閘道所用的子網。

## 示例

### 範例1：取得特定的 IP 配置
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從儲存在 $AppGw 中的閘道取得名為 GateSubnet01 的 IP 配置。

### 範例2：取得 IP 配置清單
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得所有 IP 配置的清單。

## 參數

### -ApplicationGateway
指定包含 IP 配置的應用程式閘道物件。

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
指定此 Cmdlet 取得的 IP 配置名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSApplicationGateway 中的 [.]

## 輸出

### PSApplicationGatewayIPConfiguration 中的 [.]

## 筆記

## 相關連結

[附加 AzApplicationGatewayIPConfiguration](./Add-AzApplicationGatewayIPConfiguration.md)

[新-AzApplicationGatewayIPConfiguration](./New-AzApplicationGatewayIPConfiguration.md)

[移除-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


