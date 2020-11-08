---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136253"
---
# New-AzVpnClientRevokedCertificate

## 摘要
建立新的 VPN 用戶端吊銷憑證。

## 句法

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzVpnClientRevokedCertificate** Cmdlet 會 (VPN) 用戶端吊銷憑證建立新的虛擬私人網路絡，以在虛擬網路閘道上使用。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
這個 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。
相反地，由 **New-AzVpnClientRevokedCertificate** 建立的憑證會在建立新的閘道時與 New-AzVirtualNetworkGateway Cmdlet 搭配使用。
例如，假設您建立新的憑證，並將它儲存在名為 $Certificate 的變數中。
當您建立新的虛擬閘道時，您可以使用該憑證物件。
例如， `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
如需詳細資訊，請參閱 New-AzVirtualNetworkGateway Cmdlet 的相關檔。

## 示例

### 範例1：建立新的用戶端吊銷憑證
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

這個命令會建立一個新的用戶端吊銷憑證，並將憑證物件儲存在名為 $Certificate 的變數中。
這個變數可以由 **新的-AzVirtualNetworkGateway** Cmdlet 使用，以將憑證新增到新的虛擬閘道。

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
指定新用戶端吊銷憑證的唯一名稱。

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

### -指紋
指定要新增之憑證的唯一識別碼。
您可以使用類似以下的 Windows PowerShell 命令，傳回憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root`
上述命令會傳回在根憑證存放區中找到之所有本機電腦憑證的資訊。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSVpnClientRevokedCertificate 中的 [.]

## 筆記

## 相關連結

[附加 AzVpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[移除-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


