---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: b952033bc6f04f2ed1e6d2e257dc68da1a6ec6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908845"
---
# Add-AzVpnClientRevokedCertificate

## 簡介
新增 VPN 用戶端吊銷憑證。

## 語法

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Add-Az VpnClientRevokedCertificate** Cmdlet 會指派用戶端吊銷憑證給虛擬網路閘道。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
您必須同時指定憑證名稱和憑證指紋，以使用此 Cmdlet。

## 例子

### 範例 1：新增用戶端吊銷憑證至虛擬網路閘道
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

此命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。
若要新增憑證，您必須同時指定憑證名稱和憑證指紋。

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

### -ResourceGroupName
指定指派給虛擬網路閘道的資源組名。
資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -拇指列印
指定要新增之憑證的唯一識別碼。
例如：-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 您可以使用類似以下的 Windows PowerShell 命令取得憑證的指紋 `Get-ChildItem -Path Cert:\LocalMachine\Root` 資訊。
上述命令會獲得根憑證存放區中所有找到之本地電腦憑證的資訊。

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

### -VirtualNetworkGatewayName
指定應新增憑證的虛擬網路閘道名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnClientRevokedCertificateName
指定要新增的 VPN 用戶端憑證名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate

## 筆記

## 相關連結

[Get-Az VpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[New-Az VpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-Az VpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


