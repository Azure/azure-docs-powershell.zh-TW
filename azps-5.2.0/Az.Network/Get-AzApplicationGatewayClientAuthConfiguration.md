---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: eee7040dab93a4f73bacdf440c6450a525fab9a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274168"
---
# Get-AzApplicationGatewayClientAuthConfiguration

## 摘要
取得 SSL 設定檔物件的用戶端驗證設定。

## 句法

```
Get-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzApplicationGatewayClientAuthConfiguration** Cmdlet 會取得 SSL 設定檔物件的用戶端驗證設定。

## 示例

### 範例1
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $ClientAuthConfig = Get-AzApplicationGatewayClientAuthConfiguration -SslProfile $SslProfile
```

第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。 第二個命令會針對 $AppGw 取得名為 SslProfile01 的 SSL 設定檔，並將它儲存 $SslProfile 變數。 最後一個命令會從 SSL 設定檔中取得用戶端驗證設定，$SslProfile 並將它儲存在 $ClientAuthConfig 變數中。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
Ssl 設定檔

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PSApplicationGatewaySslProfile 中的 [.]

## 輸出

### PSApplicationGatewayClientAuthConfiguration 中的 [.]

## 筆記

## 相關連結

[新-AzApplicationGatewayClientAuthConfiguration](./New-AzApplicationGatewayClientAuthConfiguration.md)

[附加 AzApplicationGatewayClientAuthConfiguration](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[移除-AzApplicationGatewayClientAuthConfiguration](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[Set-AzApplicationGatewayClientAuthConfiguration](./Set-AzApplicationGatewayClientAuthConfiguration.md)