---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3be81626dc48f66fd7aac71c23c2cd9168dab336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916021"
---
# Get-AzVpnClientIpsecParameter

## 簡介
在虛擬網路閘道上設定 vpn Ipsec 參數，以建立指向網站連接。

## 語法

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
虛擬網路閘道是代表 Azure 中閘道的物件。
**Get-Az VpnClientIpsecParameter Cmdlet** 會根據閘道名稱和資源組名，在 Azure 閘道上，會返回 vpn ipsec 參數設定的物件。

## 例子

### 範例 1：在虛擬網路閘道上設定 vpn Ipsec 參數，以建立指向網站連接。
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

會返回在虛擬網路閘道上設定 vpn ipsec 參數的物件，名稱為 "myGateway" 位於資源群組 "myRG"

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters

## 筆記

## 相關連結

[New-Az VpnClientIpsecParameter](./New-AzVpnClientIpsecParameter.md)

[Remove-Az VpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-Az VpnClientIpsecParameter](./Set-AzVpnClientIpsecParameter.md)
