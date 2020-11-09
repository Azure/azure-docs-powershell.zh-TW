---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288212"
---
# Set-AzPublicIpAddress

## 摘要
更新公用 IP 位址。

## 句法

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzPublicIpAddress** Cmdlet 會更新公用 IP 位址。

## 示例

### 1：變更公用 IP 位址的配置方法
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。
[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。
Set-AzPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。 公用 IP 位址會立即得到分配。

### 2：新增公用 IP 位址的 DNS 網域標籤
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。
[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。
Set-AzPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。 DomainNameLabel & Fqdn 會依預期修改。
    
### 3：變更公用 IP 位址的 DNS 網域標籤
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。
[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。
Set-AzPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。 DomainNameLabel & Fqdn 會依預期修改。

## 參數

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -PublicIpAddress
指定代表應該設定公用 IP 位址之狀態的公用 IP 位址物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSPublicIpAddress 中的 [.]

## 輸出

### PSPublicIpAddress 中的 [.]

## 筆記

## 相關連結

[AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[新-AzPublicIpAddress](./New-AzPublicIpAddress.md)

[移除-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)


