---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: d837355891f3b8095da0380fd91a9ac58a74acff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621897"
---
# Get-AzVpnClientIpsecParameter

## 摘要
取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。

## 句法

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
虛擬網路閘道是代表您在 Azure 中閘道的物件。
**AzVpnClientIpsecParameter** Cmdlet 會根據閘道名稱和資源組名稱，傳回在 Azure 上的閘道上設定的 vpn ipsec 參數物件。

## 示例

### 1：取得在虛擬網路閘道設定的 vpn Ipsec 參數，以指向 [網站連線]。
```
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

傳回在資源群組 "myRG" 中，以 "myGateway" 為名稱設定之 vpn ipsec 參數集的物件

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSVpnClientIPsecParameters 中的 [.]

## 筆記

## 相關連結

[新-AzVpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[移除-AzVpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-AzVpnClientIpsecParameter](./Set-AzVpnClientIpsecParameter.md)
