---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448110"
---
# Set-AzureRmNetworkSecurityGroup

## 摘要
設定網路安全性群組的目標狀態。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNetworkSecurityGroup** Cmdlet 會為 Azure 網路安全群組設定目標狀態。

## 示例

### 範例1：設定網路安全性群組的目標狀態
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

這個命令會取得名為 Nsg1 的 Azure 網路安全性群組，並將名為 Rdp-Rule 的網路安全規則，新增到使用 AzureRmNetworkSecurityRuleConfig 的 [允許埠3389上的網際網路流量]。
此命令會使用 **設定 AzureRmNetworkSecurityGroup** ，將已修改的 Azure 網路安全性群組保持不變。

## 參數

### -NetworkSecurityGroup
代表 Cmdlet 設定網路安全群組之目標狀態的網路安全群組物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSNetworkSecurityGroup
形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值

## 輸出

### PSNetworkSecurityGroup 中的 [.]

## 筆記

## 相關連結

[AzureRmNetworkSecurityGroup](./Get-AzureRmNetworkSecurityGroup.md)

[新-AzureRmNetworkSecurityGroup](./New-AzureRmNetworkSecurityGroup.md)

[移除-AzureRmNetworkSecurityGroup](./Remove-AzureRmNetworkSecurityGroup.md)


