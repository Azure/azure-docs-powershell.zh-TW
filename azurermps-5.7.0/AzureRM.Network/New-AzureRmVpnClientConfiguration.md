---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 07618d546ebdadfb3313e17b881a7afbe09d1ff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451384"
---
# New-AzureRmVpnClientConfiguration

## 摘要
這個命令可讓使用者根據 VPN 閘道預先設定的 Vpn 設定來建立 Vpn 設定檔套件，除了其他使用者可能需要設定的設定（例如，某些根憑證）。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-ProcessorArchitecture <String>] -AuthenticationMethod <String> [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這可讓使用者根據 VPN 閘道預先設定的 Vpn 設定，以及其他使用者可能需要設定的其他設定（例如，某些根憑證）來建立 Vpn 設定檔套件。

## 示例

### 範例1
```
PS C:\> New-AzureRmVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

這個 Cmdlet 是用來針對 ResourceGroup "ContosoResourceGroup" 中的 "ContosoVirtualNetworkGateway" 建立 VPN 用戶端設定檔 zip 檔案。 設定檔是針對預先設定的 radius 伺服器所產生，設定為將 "EAPTLS" 驗證方法與 VpnProfileRadiusCert 憑證檔案搭配使用。

## 參數

### -AuthenticationMethod
驗證方法可以採用值 EAPMSCHAPv2 或 EAPTLS。 指定 EAPMSCHAPv2 之後，Cmdlet 會針對使用 EAP-MSCHAPv2 驗證通訊協定的使用者名稱/密碼驗證產生用戶端配置安裝程式。 如果已指定 EAPTLS，則 Cmdlet 會針對使用 EAP-TLS 通訊協定的憑證驗證產生用戶端配置安裝程式。 "EapTls" 選項可用於以 RADIUS 為基礎的憑證驗證，以及由虛擬網路閘道上傳受信任的根所執行的認證驗證。 這個 Cmdlet 會自動偵測已設定的內容。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: EAPTLS, EAPMSCHAPv2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
用戶端根憑證路徑清單
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
資源名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RadiusRootCertificateFile
Radius 伺服器根憑證路徑。 這個強制性參數必須在使用 RADIUS 驗證的 EAP TLS 時指定。 這是 .cer 檔案的完整路徑名稱，其中包含用戶端用來驗證 RADIUS 伺服器在驗證期間的 RADIUS 根憑證。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object
[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]

## 輸出

### PSVpnProfile 中的 [.]

## 筆記

## 相關連結

