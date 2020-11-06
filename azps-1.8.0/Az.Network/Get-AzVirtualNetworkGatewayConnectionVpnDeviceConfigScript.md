---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: f4bc62c1675743c62e4e26415435d48ef52034ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621917"
---
# Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## 摘要
這個 commandlet 會採用連線資源、VPN 裝置品牌、模型、固件版本，並傳回客戶可以直接在其內部部署 VPN 裝置上套用的對應配置腳本。 此腳本將遵循所選裝置的語法，並填入 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 隧道預共用金鑰等所需的參數。客戶只需複製並貼上到其 VPN 裝置設定。

## 句法

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
這個 commandlet 會採用連線資源、VPN 裝置品牌、模型、固件版本，並傳回客戶可以直接在其內部部署 VPN 裝置上套用的對應配置腳本。 此腳本將遵循所選裝置的語法，並填入 Azure 閘道公用 IP 位址、虛擬網路位址首碼、VPN 隧道預共用金鑰等所需的參數。客戶只需複製並貼上到其 VPN 裝置設定。

## 示例

### 範例1
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

上述範例使用 Get-AzVirtualNetworkGatewaySupportedVpnDevice 來取得支援的 VPN 裝置品牌、模型及固件版本。
然後使用傳回的其中一個模型資訊，為 VirtualNetworkGatewayConnection "TestConnection" 產生 VPN 裝置配置腳本。 這個範例中所用的裝置已 DeviceFamily 「IOS-Test」、DeviceVendor 「Cisco-Test」和 FirmwareVersion 20。

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

### -DeviceFamily
VPN 裝置模型/系列的名稱。

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

### -DeviceVendor
VPN 裝置廠商的名稱。

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

### -FirmwareVersion
VPN 裝置的固件版本。

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

### -名稱
要產生設定之連接的資源名稱。

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

### -ResourceGroupName
資源群組的名稱。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### System.object

## 筆記

## 相關連結
