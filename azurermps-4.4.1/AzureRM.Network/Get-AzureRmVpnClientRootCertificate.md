---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 14fcaa1d52d2491d807e654d98308236bf901d3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448851"
---
# Get-AzureRmVpnClientRootCertificate

## 摘要
取得 VPN 根憑證的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmVpnClientRootCertificate** Cmdlet 會傳回指派給虛擬網路閘道之根憑證的相關資訊。
根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。

根據預設， **AzureRmVpnClientRootCertificate** 會傳回指派給閘道的所有根憑證的相關資訊。
 (閘道可以有一個以上的根憑證。 ) 不過，透過包括 **VpnClientRootCertificateName** 參數，您可以將傳回的資料限制為特定的憑證。

## 示例

### 範例1：取得所有根憑證的相關資訊
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

這個命令會取得指派給名為 ContosoVirtualNetwork 的虛擬網路閘道所有根憑證的相關資訊。

### 範例2：取得特定根憑證的相關資訊
```
PS C:\>Get-AzureRmVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

這個命令是範例1中所示命令的變化。
但在此情況下，會包含 *VpnClientRootCertificateName* 參數，以便將傳回的資料限制為特定的根憑證： ContosoRootClientCertificate。

## 參數

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

### -VirtualNetworkGatewayName
指定指派根憑證之虛擬網路閘道的名稱。

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

### -VpnClientRootCertificateName
指定此 Cmdlet 所取得之用戶端根憑證的名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

###  
**AzureRmVpnClientRootCertificate** 會取得 PSVpnClientRootCertificate 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** 物件）。

## 筆記

## 相關連結

[附加 AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[新-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)

[移除-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


