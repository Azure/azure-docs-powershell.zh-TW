---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 3ebe90d5f28adf0e7e4a9de66b04a1ea000cc69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449304"
---
# Get-AzureRmApplicationGatewayIPConfiguration

## 摘要
取得應用程式閘道的 IP 配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmApplicationGatewayIPConfiguration** Cmdlet 會取得應用程式閘道的 IP 配置。
[IP 設定] 包含部署應用程式閘道所用的子網。

## 示例

### 範例1：取得特定的 IP 配置
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從儲存在 $AppGw 中的閘道取得名為 GateSubnet01 的 IP 配置。

### 範例2：取得 IP 配置清單
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得所有 IP 配置的清單。

## 參數

### -ApplicationGateway
指定包含 IP 配置的應用程式閘道物件。

```yaml
Type: PSApplicationGateway
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 取得的 IP 配置名稱。

```yaml
Type: String
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

### System.object

## 輸出

### PSApplicationGatewayIPConfiguration 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmApplicationGatewayIPConfiguration](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[新-AzureRmApplicationGatewayIPConfiguration](./New-AzureRmApplicationGatewayIPConfiguration.md)

[移除-AzureRmApplicationGatewayIPConfiguration](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[Set-AzureRmApplicationGatewayIPConfiguration](./Set-AzureRmApplicationGatewayIPConfiguration.md)


