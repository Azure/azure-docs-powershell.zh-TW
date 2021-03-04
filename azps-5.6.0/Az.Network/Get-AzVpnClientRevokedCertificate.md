---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901974"
---
# Get-AzVpnClientRevokedCertificate

## 簡介
獲得 VPN 用戶端吊銷憑證相關資訊。

## 語法

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-Az VpnClientRevokedCertificate** Cmdlet 會返回指派給虛擬網路閘道的用戶端吊銷憑證相關資訊。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
**Get-Az VpnClientRevokedCertificate** 可讓您返回閘道上所有用戶端吊銷憑證的資訊，或使用 *VpnClientRevokedCertificateName* 參數取得單一憑證的資訊。

## 例子

### 範例 1：取得所有用戶端吊銷憑證的資訊
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

此命令會獲得與名為 ContosoVirtualNetworkGateway 之虛擬網路閘道相關聯的所有用戶端吊銷憑證相關資訊。

### 範例 2：取得特定用戶端吊銷憑證的資訊
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

此命令是範例 1 中顯示的命令變化。
不過，在此案例中 *，VpnClientRevokedCertificateName* 參數是用來將所退回的資料限制為特定的用戶端撤銷憑證：名稱為 ContosoRevokedClientCertificate 的憑證。

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

### -VirtualNetworkGatewayName
指定指派已撤銷憑證資訊的虛擬網路閘道名稱。

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
指定此 Cmdlet 所獲得 VPN 用戶端憑證的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate

## 筆記

## 相關連結

[Add-Az VpnClientRevokedCertificate](./Add-AzVpnClientRevokedCertificate.md)

[New-Az VpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[Remove-Az VpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


