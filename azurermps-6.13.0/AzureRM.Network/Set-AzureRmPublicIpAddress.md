---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: ed3b2de22c5f71c0782724f99c8325de4dea98b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448300"
---
# Set-AzureRmPublicIpAddress

## 摘要
設定公用 IP 位址的目標狀態。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmPublicIpAddress** Cmdlet 設定公用 IP 位址的目標狀態。

## 示例

### 1：變更公用 IP 位址的配置方法
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。
[第二個] 命令會將公用 IP 位址物件的配置方法設定為「靜態」。
Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源，並將分攤方法修改為 [Static "。 公用 IP 位址會立即得到分配。

### 2：變更公用 IP 位址的 DNS 網域標籤
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

第一個命令會在資源群組 $rgName 中取得名稱 $publicIPName 的公用 IP 位址資源。
[第二個] 命令會將 DomainNameLabel 屬性設為所需的 dns 前置詞。
Set-AzureRmPublicIPAddress 命令會以更新的物件更新公用 IP 位址資源。 DomainNameLabel & Fqdn 會依預期修改。

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddress
指定代表應該設定公用 IP 位址之目標狀態的 **PublicIpAddress** 物件。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSPublicIpAddress 中的 [.]
參數： PublicIpAddress (ByValue) 

## 輸出

### PSPublicIpAddress 中的 [.]

## 筆記

## 相關連結

[AzureRmPublicIpAddress](./Get-AzureRmPublicIpAddress.md)

[新-AzureRmPublicIpAddress](./New-AzureRmPublicIpAddress.md)

[移除-AzureRmPublicIpAddress](./Remove-AzureRmPublicIpAddress.md)


