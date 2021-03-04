---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915930"
---
# Remove-AzVpnClientRootCertificate

## 簡介
移除現有的 VPN 用戶端根憑證。

## 語法

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Remove-Az VpnClientRootCertificate** Cmdlet 會從虛擬網路閘道移除指定的根憑證。
根憑證是 X.509 憑證，可識別您的根憑證授權單位憑證授權單位機關：閘道中使用的所有其他憑證都根信任憑證。
如果您移除的根憑證電腦若將憑證用於驗證用途，就無法再連接到閘道。
當您使用 **Remove-Az VpnClientRootCertificate** 時，您必須同時提供憑證名稱和憑證資料的文字標記法。
有關憑證的文字表示方式詳細資訊，請參閱 *PublicCertData* 參數描述。

## 例子

### 範例 1：從虛擬網路閘道移除用戶端根憑證
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

此範例會從虛擬網路閘道 ContosoVirtualGateway 移除名為 ContosoRootCertificate 的用戶端根憑證。
第一個命令使用 **Get-Content** Cmdlet 取得先前匯出之憑證的文字標記法;此文字標記法會儲存在名為 $Text 的$Text。
接著，第二個命令會使用 for loop 來解壓縮$Text除了第一行和最後一行以外。
此解壓縮的文字會儲存在名為 $CertificateText 的變數中。
第三個命令會使用 $CertificateText 變數中儲存的資訊以及 **Remove-Az VpnClientRootCertificate** Cmdlet，以從閘道移除憑證。

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
指定要移除之根憑證的文字標記法。
若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64) 編碼，然後在文字編輯器中開啟產生的檔案。
您應該會看到類似下列輸出 (請注意，實際輸出包含的文字行數會比此處顯示的縮寫範例更多) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。
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
指定從中移除憑證的虛擬網路閘道名稱。

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
指定此 Cmdlet 移除的用戶端根憑證名稱。

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

[Add-Az VpnClientRootCertificate](./Add-AzVpnClientRootCertificate.md)

[Get-Az VpnClientRootCertificate](./Get-AzVpnClientRootCertificate.md)

[New-Az VpnClientRootCertificate](./New-AzVpnClientRootCertificate.md)


