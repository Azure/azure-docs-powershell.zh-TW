---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142233"
---
# Add-AzVpnClientRevokedCertificate

## 摘要
新增 VPN 用戶端吊銷憑證。

## 句法

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證指派給虛擬網路閘道。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
您必須指定憑證名稱和憑證指紋，才能使用此 Cmdlet。

## 示例

### 範例1：將新的用戶端吊銷憑證新增至虛擬網路閘道
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

這個命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。
若要新增憑證，您必須指定憑證名稱和憑證指紋。

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

### -ResourceGroupName
指定指派虛擬網路閘道之資源群組的名稱。
資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。

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

### -指紋
指定要新增之憑證的唯一識別碼。
例如：-指紋 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 您可以使用類似以下的 Windows PowerShell 命令來取得憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root` 。
上述命令會取得在根憑證存放區中找到之所有本機電腦憑證的資訊。

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
指定要新增憑證的虛擬網路閘道名稱。

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
指定要新增之 VPN 用戶端憑證的名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSVpnClientRevokedCertificate 中的 [.]

## 筆記

## 相關連結

[AzVpnClientRevokedCertificate](./Get-AzVpnClientRevokedCertificate.md)

[新-AzVpnClientRevokedCertificate](./New-AzVpnClientRevokedCertificate.md)

[移除-AzVpnClientRevokedCertificate](./Remove-AzVpnClientRevokedCertificate.md)


