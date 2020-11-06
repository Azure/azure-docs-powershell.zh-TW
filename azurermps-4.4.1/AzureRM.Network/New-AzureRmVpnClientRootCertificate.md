---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 941be726f2b7c7aaf3ebf3d4cef0a91239e88214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446722"
---
# New-AzureRmVpnClientRootCertificate

## 摘要
建立新的 VPN 用戶端根憑證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmVpnClientRootCertificate** Cmdlet 會建立新的 VPN 根憑證，以用於虛擬網路閘道。
根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。

這個 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。
相反地，由 **New-AzureRmVpnClientRootCertificate** 建立的憑證會與建立新閘道時的 New-AzureRmVirtualNetworkGateway Cmdlet 搭配使用。
例如，假設您建立新的憑證，並將它儲存在名為 $Certificate 的變數中。
在建立新的虛擬閘道時，您可以使用該憑證物件。
例如，

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

如需詳細資訊，請參閱 New-AzureRmVirtualNetworkGateway Cmdlet 的相關檔。

## 示例

### 範例1：建立 aclient 根憑證
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

這個範例會建立一個用戶端根憑證，並將憑證物件儲存在名為 $Certificate 的變數中。
這個變數可以由 **新的-AzureRmVirtualNetworkGateway** Cmdlet 使用，以將根憑證新增至新的虛擬閘道。

第一個命令使用 **取得內容** Cmdlet 來取得根憑證先前匯出的文字標記法;該文字資料會儲存在名為 $Text 的變數中。

然後，第二個命令會使用 for 迴圈來提取除了第一行和最後一行以外的所有文字，並將提取的文字儲存在名為 $CertificateText 的變數中。

第三個命令使用 **AzureRmVpnClientRootCertificate** Cmdlet 來建立證書，並將建立的物件儲存在名為 $Certificate 的變數中。

## 參數

### -名稱
指定新用戶端根憑證的名稱。

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

### -PublicCertData
指定要新增之根憑證的文字標記法。
若要取得文字標記法，請 (使用 Base64 編碼) 將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。
您應該會看到類似這個 (的輸出，請注意，實際的輸出會包含許多其他行的文字，而不是此處顯示的縮寫範例) ：

-----開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----[結束憑證]-----

PublicCertData 是由第一行之間的所有行所 (-----[開始憑證-----) ，而最後一行 (-----在檔案中-----[最終憑證 ) 。
您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData：

$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }

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

###  
這個 Cmdlet 不接受流水線輸入。

## 輸出

###  
這個 Cmdlet 會建立 PSVpnClientRootCertificate 物件的新實例（ **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** 物件）。

## 筆記

## 相關連結

[附加 AzureRmVpnClientRootCertificate](./Add-AzureRmVpnClientRootCertificate.md)

[AzureRmVpnClientRootCertificate](./Get-AzureRmVpnClientRootCertificate.md)

[移除-AzureRmVpnClientRootCertificate](./Remove-AzureRmVpnClientRootCertificate.md)


