---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399391"
---
# Get-AzVpnClientPackage

## 簡介
獲得 VPN 用戶端套件相關資訊。

## 語法

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-Az VpnClientPackage Cmdlet** 會取得來自虛擬網路閘道的 VPN 用戶端套件相關資訊。
用戶端套件包含可讓用戶端電腦進行 Azure 虛擬網路的 VPN 連接之組配置資料;用戶端電腦必須安裝正確的組組套件，才能建立 VPN 連接。
根據用戶端電腦版本的 Windows (例如 Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 提供不同的組組套件。
您必須先指定架構類型，才能進行 **Get-Az VpnClientPackage。**

## 例子

### 範例 1：取得有關處理器架構 VPN 用戶端套件的資訊
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

此命令會獲得儲存在名為 ContosoVirtualNetworkGateway 之虛擬網路閘道上的 AMD64 VPN 用戶端套件相關資訊。
若要取得 x86 用戶端套件相關資訊，請設定 *處理器Architecture* 參數的值為 x86。

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

### -ProcessorArchitecture
指定用戶端套件所設計的 CPU 架構類型。
有效的值為Amd64 和 X86。

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
指定指派給虛擬網路閘道的資源組名。
資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。

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
指定儲存用戶端套件資訊的虛擬網路閘道名稱。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### System.String

## 筆記

## 相關連結

[Resize-AzVirtualNetworkGateway](./Resize-AzVirtualNetworkGateway.md)



