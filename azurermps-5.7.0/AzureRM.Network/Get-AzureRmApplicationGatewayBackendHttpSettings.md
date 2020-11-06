---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449866"
---
# Get-AzureRmApplicationGatewayBackendHttpSettings

## 摘要
取得應用程式閘道的後端 HTTP 設定。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 會取得應用程式閘道的後端 HTTP 設定。

## 示例

### 範例1：依名稱取得後端 HTTP 設定
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會針對 $AppGw 取得名為 Settings01 的 HTTP 設定，並將設定儲存在 $Settings 變數中。

### 範例2：取得後端 HTTP 設定集合
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得 $AppGw 的 HTTP 設定集合，並將設定儲存在 $SettingsList 變數中。

## 參數

### -ApplicationGateway
指定包含後端 HTTP 設定的應用程式閘道物件。

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
指定此 Cmdlet 所取得之後端 HTTP 設定的名稱。

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

### AzureApplicationGatewayBackendHttpSettings 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmApplicationGatewayBackendHttpSettings]()

[新-AzureRmApplicationGatewayBackendHttpSettings]()

[移除-AzureRmApplicationGatewayBackendHttpSettings]()

[Set-AzureRmApplicationGatewayBackendHttpSettings]()

