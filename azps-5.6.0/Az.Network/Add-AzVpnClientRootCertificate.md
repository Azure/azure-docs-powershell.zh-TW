---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908837"
---
# Add-AzVpnClientRootCertificate

## 簡介
新增 VPN 用戶端根憑證。

## 語法

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Add-Az VpnClientRootCertificate** Cmdlet 會將根憑證新增到虛擬網路閘道。
根憑證是 X.509 憑證，可識別您的根憑證授權單位。
根據設計，閘道上使用的所有憑證都根信任憑證。
此 Cmdlet 會指派現有憑證做為閘道根憑證。
如果您沒有可用的 X.509 憑證，您可以透過公用金鑰基礎結構產生一個憑證，或使用憑證產生器 ，例如 makecert.exe。
若要新增根憑證，您必須指定憑證名稱，並提供憑證的純文字表示 (請參閱 *PublicCertData* 參數以) 。
Azure 可讓您將多個根憑證指派給閘道。
多個根憑證通常是由包含多個公司使用者的組織所部署。

## 例子

### 範例 1：新增用戶端根憑證至虛擬閘道
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

此範例會將用戶端根憑證新增到名為 ContosoVirtualGateway 的虛擬閘道。
第一個命令使用 **Get-Content** Cmdlet 取得先前匯出的根憑證文字標記法，並儲存名為 $Text 的變數之文字資料。
接著，第二個命令會使用 for loop 來抽選第一行和最後一行以外的所有文字。
解壓縮的文字會儲存在名為 $CertificateText 的$CertificateText。
接著，第三個命令會使用儲存在 $CertificateText 中的文字與 **Add-Az VpnClientRootCertificate** Cmdlet，將根憑證新增到閘道。

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

### -PublicCertData
指定要新增之根憑證的文字標記法。
若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64 編碼) ，然後在文字編輯器中開啟產生的檔案。
當您這麼做時，會看到類似下列的 (請注意，實際輸出的文字行數會比此處顯示的縮寫範例多出許多行文字) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8 343NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。
您可以使用類似以下的 Windows PowerShell 命令來取回此資料： `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
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
指定根憑證指派給的資源組名。
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
指定此 Cmdlet 新增的用戶端根憑證名稱。

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

### Microsoft.Azure.Commands.Network.models.PS VpnClientRootCertificate

## 筆記

## 相關連結

[Get-Az VpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-Az VpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)

[Remove-Az VpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


