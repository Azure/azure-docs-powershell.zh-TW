---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 1a38c55757f96b99a6801452f490f0fc4240fde1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790238"
---
# Add-AzVpnClientRootCertificate

## 摘要
新增 VPN 用戶端根憑證。

## 句法

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**載入 AzVpnClientRootCertificate** Cmdlet 會將根憑證新增至虛擬網路閘道。
根憑證是 x.509 可識別您根憑證授權單位的憑證。
根據設計，在閘道上使用的所有憑證都根信任憑證。
這個 Cmdlet 會將現有的憑證指派為閘道根憑證。
如果您沒有可用的 x.509 憑證，您可以透過公開金鑰基礎結構產生一個證書，或使用證書發生器（例如 makecert.exe）。
若要新增根憑證，您必須指定憑證名稱並提供憑證的純文字標記法 (請參閱 *PublicCertData* 參數，以取得詳細資訊) 。
Azure 可讓您將一個以上的根憑證指派給閘道。
多個根憑證通常是由組織加入來自多個公司的使用者所部署。

## 示例

### 範例1：將用戶端根憑證新增至虛擬閘道
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

這個範例會將用戶端根憑證新增到名為 ContosoVirtualGateway 的虛擬閘道。
第一個命令會使用 **取得內容** Cmdlet 來取得根憑證先前匯出的文字標記法，並將該文字資料儲存在名為 $Text 的變數。
然後，第二個命令會使用 for 迴圈來提取除第一行和最後一行以外的所有文字。
解壓縮的文字會儲存在名為 $CertificateText 的變數中。
然後，第三個命令會使用儲存在 $CertificateText 中的文字與 **AzVpnClientRootCertificate** Cmdlet，以將根憑證新增至閘道。

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

### -PublicCertData
指定要新增之根憑證的文字標記法。
若要取得文字標記法，請 (使用 Base64 編碼) 將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。
當您這樣做時，您會看到類似下列 (的輸出，請注意，實際輸出會包含多行文字，而不是) 以下所示的縮寫範例：-----[開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----[結束憑證]----- ( 的 [開始憑證----------，而最後一行 )  ( 在檔案中-----最終憑證-----。
您可以使用類似以下的 Windows PowerShell 命令來檢索這個資料： `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`

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

### -ResourceGroupName
指定指派根憑證之資源群組的名稱。
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
指定新增憑證的虛擬網路閘道名稱。

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
指定此 Cmdlet 所新增之用戶端根憑證的名稱。

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

### PSVpnClientRootCertificate 中的 [.]

## 筆記

## 相關連結

[AzVpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[新-AzVpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[移除-AzVpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


