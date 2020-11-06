---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: e9095c5f2e8f2a9820214f1144f10f8049f22027
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447335"
---
# Remove-AzureRmVpnClientRevokedCertificate

## 摘要
移除 VPN 用戶端吊銷憑證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證從虛擬網路閘道中移除。
用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。
如果您移除用戶端吊銷憑證用戶端電腦，就可以使用先前禁止的憑證，將虛擬私人網路 (VPN) 連線。

## 示例

### 範例1：從虛擬網路閘道移除用戶端吊銷憑證
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

這個命令會從名為 ContosoVirtualNetwork 的虛擬網路閘道中移除用戶端吊銷憑證。
若要移除用戶端吊銷憑證，您必須指定憑證名稱和憑證指紋。

## 參數

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
指定要移除之憑證的唯一識別碼。
您可以使用類似以下的 Windows PowerShell 命令，傳回憑證的指紋資訊： `Get-ChildItem -Path "Cert:\LocalMachine\Root"`
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

### -VirtualNetworkGatewayName
指定指派憑證的虛擬網路閘道的名稱。

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
指定要移除之 VPN 用戶端憑證的名稱。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### System.object

## 筆記

## 相關連結

[附加 AzureRmVpnClientRevokedCertificate](./Add-AzureRmVpnClientRevokedCertificate.md)

[AzureRmVpnClientRevokedCertificate](./Get-AzureRmVpnClientRevokedCertificate.md)

[新-AzureRmVpnClientRevokedCertificate](./New-AzureRmVpnClientRevokedCertificate.md)


