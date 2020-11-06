---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 92e1f701eb9d0eafdea72ba031a7799c7c0adbce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446943"
---
# Remove-AzureRmApplicationGatewayConnectionDraining

## 摘要
移除後端 HTTP 設定物件的連接排出配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmApplicationGatewayConnectionDraining** Cmdlet 會移除後端 HTTP 設定物件的連接排出配置。

## 示例

### 範例1
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。
第二個命令會針對 $AppGw 取得名為 Settings01 的後端 HTTP 設定，並將設定儲存在 $Settings 變數中。
最後一個命令會移除 $Settings 中儲存後端 HTTP 設定的連接排出設定。

## 參數

### -BackendHttpSettings
後端 HTTP 設定

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSApplicationGatewayBackendHttpSettings 中的 [.]
參數： BackendHttpSettings (ByValue) 

## 輸出

### PSApplicationGatewayBackendHttpSettings 中的 [.]

## 筆記

## 相關連結

[AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[AzureRmApplicationGatewayBackendHttpSettings](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[AzureRmApplicationGatewayConnectionDraining](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[新-AzureRmApplicationGatewayConnectionDraining](./New-AzureRmApplicationGatewayConnectionDraining.md)

[Set-AzureRmApplicationGatewayConnectionDraining](./Set-AzureRmApplicationGatewayConnectionDraining.md)

