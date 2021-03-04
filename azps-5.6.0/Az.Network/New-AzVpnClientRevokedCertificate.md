---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904946"
---
# New-AzVpnClientRevokedCertificate

## 簡介
建立新的 VPN 用戶端吊銷憑證。

## 語法

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-Az VpnClientRevokedCertificate Cmdlet** 會建立新的虛擬私人網路 (VPN) 用戶端吊銷憑證，以用於虛擬網路閘道。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
此 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。
相反地 **，New-Az VpnClientRevokedCertificate** 所建立憑證在建立新閘道時，會與 New-AzVirtualNetworkGateway Cmdlet 一起使用。
例如，假設您建立新憑證，然後儲存在名為 $Certificate 的變數中。
然後，您可以在建立新虛擬閘道時使用該憑證物件。
例如， `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`
詳細資訊請參閱 Cmdlet New-AzVirtualNetworkGateway檔。

## 例子

### 範例 1：建立新的用戶端撤銷憑證
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

此命令會建立新的用戶端撤銷憑證，並且將憑證物件儲存在名為 $Certificate 的變數中。
**New-AzVirtualNetworkGateway** Cmdlet 接著可以使用這個變數，將憑證新增到新的虛擬網路閘道。

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

### -名稱
指定新的用戶端吊銷憑證的唯一名稱。

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

### -拇指列印
指定要新增之憑證的唯一識別碼。
您可以使用類似以下的 Windows PowerShell 命令，針對憑證返回指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root`
上一個命令會針對根憑證存放區中找到的所有 Local Computer 憑證，會返回資訊。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate

## 筆記

## 相關連結

[Add-Az VpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-Az VpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[Remove-Az VpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


