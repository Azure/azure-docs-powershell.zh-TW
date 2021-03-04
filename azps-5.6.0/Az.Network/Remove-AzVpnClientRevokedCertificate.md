---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: d7665d490979ca15189650572c083a94efb6c123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915342"
---
# Remove-AzVpnClientRevokedCertificate

## 簡介
移除 VPN 用戶端吊銷憑證。

## 語法

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Remove-Az VpnClientRevokedCertificate Cmdlet** 會從虛擬網路閘道移除用戶端吊銷憑證。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
如果您移除用戶端吊銷憑證，用戶端電腦就可以使用先前禁止的憑證，讓虛擬私人網路 (VPN) 連接。

## 例子

### 範例 1：從虛擬網路閘道移除用戶端吊銷憑證
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

此命令會從名為 ContosoVirtualNetwork 的虛擬網路閘道移除用戶端吊銷憑證。
若要移除用戶端吊銷憑證，您必須同時指定憑證名稱和憑證指紋。

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
指定要移除之憑證的唯一識別碼。
您可以使用類似以下的 Windows PowerShell 命令，針對憑證返回指紋資訊： `Get-ChildItem -Path "Cert:\LocalMachine\Root"`
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

### -VirtualNetworkGatewayName
指定憑證指派給的虛擬網路閘道名稱。

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
指定要移除的 VPN 用戶端憑證名稱。

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

### System.Boolean

## 筆記

## 相關連結

[Add-Az VpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[Get-Az VpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[New-Az VpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)


