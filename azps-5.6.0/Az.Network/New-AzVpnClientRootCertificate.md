---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904945"
---
# New-AzVpnClientRootCertificate

## 簡介
建立新的 VPN 用戶端根憑證。

## 語法

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-Az VpnClientRootCertificate Cmdlet** 會建立新 VPN 根憑證，以用於虛擬網路閘道。
根憑證是 X.509 憑證，可識別您的根憑證授權單位憑證授權單位機關：閘道中使用的所有其他憑證都根信任憑證。
此 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。
相反地 **，New-Az VpnClientRootCertificate** 所建立憑證會與 New-AzVirtualNetworkGateway Cmdlet 一起使用，以建立新閘道。
例如，假設您建立新憑證，然後儲存在名為 $Certificate 的變數中。
接著，您可以在建立新虛擬閘道時使用該憑證物件。
例如， `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`
詳細資訊請參閱 Cmdlet New-AzVirtualNetworkGateway檔。

## 例子

### 範例 1：建立用戶端根憑證
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

此範例會建立用戶端根憑證，並儲存在名為 $Certificate 的變數中。
**New-AzVirtualNetworkGateway** Cmdlet 接著可以使用這個變數，將根憑證新增加到新的虛擬網路閘道。
第一個命令使用 **Get-Content** Cmdlet 取得先前匯出之根憑證的文字標記法;文字資料會儲存在名為 $Text 的變數中。
接著，第二個命令使用 for loop 來抽選第一行和最後一行以外的所有文字，將解壓縮的文字儲存于名為 $CertificateText 的變數中。
第三個命令使用 **New-Az VpnClientRootCertificate Cmdlet** 建立憑證，將建立的物件儲存于名為 $Certificate 的變數中。

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
若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64 編碼) ，然後在文字編輯器中開啟產生的檔案。
您應該會看到類似此輸出 (請注意，實際輸出包含的文字行數會比此處顯示的縮寫範例更多) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW834 3NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。
您可以使用類似以下的 Windows PowerShell 命令來取回 PublicCertData：$Text = Get-Content -Path "C：\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1;$i -lt $Text.Length -1 ;$i++) {$Text$i \[ \] }

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientRootCertificate

## 筆記

## 相關連結

[Add-Az VpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-Az VpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[Remove-Az VpnClientRootCertificate](./Remove-AzVpnClientRootCertificate.md)


