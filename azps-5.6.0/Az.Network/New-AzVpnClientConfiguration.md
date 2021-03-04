---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904953"
---
# New-AzVpnClientConfiguration

## 簡介
此命令可讓使用者根據 VPN 閘道上預先設定 vpn 設定建立 Vpn 設定檔套件，以及使用者可能需要設定的其他設定，例如一些根憑證。

## 語法

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 描述
這可讓使用者根據 VPN 閘道上預先設定 VPN 設定建立 Vpn 設定檔套件，以及一些使用者可能需要設定的其他設定，例如一些根憑證。

## 例子

### 範例 1
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

此 Cmdlet 用於為 ResourceGroup "ContosoResourceGroup" 中的 "ContosoVirtualNetworkGateway" 建立 VPN 用戶端設定檔 zip 檔案。 設定檔的產生位置為預先配置的弧形伺服器，該伺服器已針對 VpnProfileRadiusCert 憑證檔案使用 "EAPTLS" 驗證方法。

## 參數

### -AuthenticationMethod
驗證方法可以取值 EAPMSCHAPv2 或 EAPTLS。 指定 EAPMSCHAPv2 時，Cmdlet 會針對使用驗證通訊協定的使用者名稱/密碼驗證產生EAP-MSCHAPv2安裝程式。 如果指定 EAPTLS，Cmdlet 會針對使用 EAP-TLS 通訊協定的憑證驗證產生用戶端組組安裝程式。 「EapTls」選項可用來上傳信任的根目錄，同時用於以 RADIUS 為基礎的憑證驗證，以及由虛擬網路閘道執行的認證驗證。 Cmdlet 會自動偵測到已配置哪些專案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ClientRootCertificateFileList
用戶端根憑證路徑清單

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
資源名稱。

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

### -ProcessorArchitecture
ProcessorArchitecture

```yaml
Type: System.String
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
弧線伺服器根憑證路徑。 這是使用具有 RADIUS 驗證的 EAP-TLS 時必須指定的強制參數。 這是 .cer 檔案的完整路徑名稱，其中包含在驗證期間用戶端用來驗證 RADIUS 伺服器之 RADIUS 根憑證。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名。

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

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### System.String[]

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnProfile

## 筆記

## 相關連結

[Get-Az VpnClientConfiguration](./Get-AzVpnClientConfiguration.md)
