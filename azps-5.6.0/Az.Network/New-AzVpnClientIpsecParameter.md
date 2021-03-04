---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913145"
---
# New-AzVpnClientIpsecParameter

## 簡介
此命令可讓使用者建立 Vpn ipsec 參數物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。

## 語法

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
此命令可讓使用者建立 Vpn ipsec 參數物件，指定一或所有值，例如 IpsecEncryption、IpsecIntegrity、IkeEncryption、IkeIntegrity、DhGroup、PfsGroup，以在現有的 VPN 閘道上設定。

## 例子

### 範例 1
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

New-AzVpnClientIpsecParameter Cmdlet 用來建立 vpn ipsec 參數物件，使用使用者可針對 ResourceGroup 中任何現有虛擬網路閘道所設定之傳遞的一或所有參數值。
此建立 VpnClientIPsecParameters 物件會傳遞至 Set-AzVpnClientIpsecParameter 命令，以在虛擬網路閘道上設定指定的 Vpn ipsec 自訂策略，如上述範例所示。 此命令會返回 VpnClientIPsecParameters 的物件，該物件會顯示 set 參數。

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

### -DhGroup
用於 IKE 階段 1 初始 SA 的 VpnClient DH 群組。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeEncryption
IKE 階段 2 (的 VpnClient IKE 加密演算法) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IkeIntegrity
IKE 階段 2 (的 VpnClient IKE 完整性演算法) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecEncryption
IKE 階段 1 (中的 VpnClient IPSec 加密演算法) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpsecIntegrity
IKE 階段 1 (的 VpnClient IPSec 完整性演算法) 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PfsGroup
新子 SA 在 IKE 階段 2 中使用的 VpnClient PFS 群組

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SADataSize
VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA) KB 的負載大小

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SALifeTime
VpnClient IPSec 安全性關聯 (稱為快速模式或階段 2 SA 生命週期) 秒

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PS VpnClientIPsecParameters

## 筆記

## 相關連結

[Get-Az VpnClientIpsecParameter](./Get-AzVpnClientIpsecParameter.md)

[Remove-Az VpnClientIpsecParameter](./Remove-AzVpnClientIpsecParameter.md)

[Set-Az VpnClientIpsecParameter](./Set-AzVpnClientIpsecParameter.md)
