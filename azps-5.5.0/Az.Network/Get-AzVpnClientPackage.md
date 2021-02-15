---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: 8eba8d26bcac5de16be3e2cda5e8ca80356aea11
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134971"
---
# Get-AzVpnClientPackage

## 摘要
取得 VPN 用戶端套件的相關資訊。

## 句法

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzVpnClientPackage** Cmdlet 會取得虛擬網路閘道提供之 VPN 用戶端套件的相關資訊。
用戶端套件包含可讓用戶端電腦建立 Azure 虛擬網路 VPN 連線的配置資料;用戶端電腦必須安裝正確的 configuration 套件，才能進行 VPN 連線。
根據用戶端電腦的 Windows 版本，您可以使用不同的配置套件 (例如，Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 。
在執行 **AzVpnClientPackage** 時，您必須指定架構類型。

## 示例

### 範例1：取得處理器架構 VPN 用戶端套件的相關資訊
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

這個命令會取得 AMD64 VPN 用戶端套件的相關資訊，這些元件儲存在名為 ContosoVirtualNetworkGateway 的虛擬網路閘道。
若要取得 x86 用戶端套件的相關資訊，請將 *ProcessorArchitecture* 參數的值設定為 x86。

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

### -ProcessorArchitecture
指定用戶端套件所設計的 CPU 架構類型。
有效值為 Amd64 和 X86。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

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
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkGatewayName
指定儲存用戶端套件資訊之虛擬網路閘道的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### System.object

## 筆記

## 相關連結

[調整大小-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


