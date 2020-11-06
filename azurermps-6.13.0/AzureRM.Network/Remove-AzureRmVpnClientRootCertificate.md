---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 95442c724548119726aa466edf1b4fa223271865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455976"
---
# Remove-AzureRmVpnClientRootCertificate

## 摘要
移除現有的 VPN 用戶端根憑證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmVpnClientRootCertificate** Cmdlet 會將指定的根憑證從虛擬網路閘道中移除。
根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。
如果您移除使用憑證進行驗證的根憑證電腦，將無法再連線至閘道。
當您使用 **AzureRmVpnClientRootCertificate** 時，您必須同時提供憑證名稱和憑證資料的文字標記法。
如需有關憑證之文字標記法的詳細資訊，請參閱 *PublicCertData* 參數說明。

## 示例

### 範例1：從虛擬網路閘道移除用戶端根憑證
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

這個範例會從虛擬網路閘道 ContosoVirtualGateway 中移除名為 ContosoRootCertificate 的用戶端根憑證。
第一個命令使用 **取得內容** Cmdlet 來取得前一次匯出的憑證文字標記法;此文字標記法儲存在名為 $Text 的變數中。
然後，第二個命令會使用 for 迴圈來提取 $Text 中除第一行和最後一行以外的所有文字。
這個提取的文字會儲存在名為 $CertificateText 的變數中。
第三個命令會使用儲存在 $CertificateText 變數中的資訊，以及 **AzureRmVpnClientRootCertificate** Cmdlet 來移除閘道的憑證。

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

### -PublicCertData
指定要移除之根憑證的文字標記法。
若要取得文字標記法，請 (使用 Base64) 編碼將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。
您應該會看到類似 (如下所示的輸出，請注意，實際輸出會包含的文字行多於以下所示的縮寫範例) ：-----的開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----結束憑證----- ( 開始憑證----------，而最後一行 )  ( 在檔案中-----最終憑證-----) 。
您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData： $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }

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
指定從中移除憑證的虛擬網路閘道的名稱。

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
指定此 Cmdlet 移除之用戶端根憑證的名稱。

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

[附加 AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[新-AzureRmVpnClientRootCertificate](./New-AzureRmVpnClientRootCertificate.md)


