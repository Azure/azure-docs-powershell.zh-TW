---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9273c4cf6d23825b931dda696e1a2ef8513aa68d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788969"
---
# Set-AzNetworkInterface

## 摘要
更新網路介面。

## 句法

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzNetworkInterface** 會更新網路介面。

## 示例

### 範例1：設定網路介面
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

這個範例會設定網路介面。
第一個命令會在資源群組 ResourceGroup1 中取得名為 NetworkInterface1 的網路介面。
第二個命令會設定 IP 配置的私人 IP 位址。
第三個命令會將專用 IP 配置方法設定為 Static。
第四個命令會在網路介面上設定標記。
第五個命令使用儲存在 $Nic 變數中的資訊來設定網路介面。

### 範例2：變更網路介面上的 DNS 設定
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的網路介面，該網路介面存在於資源群組 ResourceGroup1 中。 第二個命令會將 DNS 伺服器192.168.1.100 新增到這個介面。 第三個命令會將這些變更套用至網路介面。 若要移除 DNS 伺服器，請遵循上面所列的命令，但要取代 "。新增 "with"。第二個命令中的 [移除]。

### 範例3：在網路介面上啟用 IP 轉寄
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。 第二個命令會將 IP 轉寄值變更為 true。 最後，第三個命令會將變更套用至網路介面。 若要在網路介面上停用 IP 轉寄功能，請遵循範例範例，但務必將第二個命令改為「$nic。EnableIPForwarding = 0 "。

### 範例4：變更網路介面的子網
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

第一個命令會取得網路介面 NetworkInterface1，並將它儲存在 $nic 變數中。 第二個命令會取得與網路介面將要關聯之子網相關聯的虛擬網路。 第二個命令會取得子網，並將它儲存在 $subnet 2 變數中。 第三個命令會將網路介面的主要私人 IP 位址與新的子網相關聯。 最後，最後一個命令會在網路介面上套用這些變更。
>[!NOTE] 
>您必須先動態使用 IP 設定，才能變更子網。 如果您有靜態 IP 設定，請先將它變更為 [動態]，然後再繼續進行。 
>[!NOTE]
>如果網路介面有多個 IP 設定，則在執行最後一個 Set-AzNetworkInterface 命令之前，必須完成所有這些 IP 設定的第四個命令。 您可以在第四個命令中完成，但將 "0" 取代為適當的數位。 如果網路介面具有 N 個 IP 配置，則必須存在這些命令的 N-1。

### 範例5：將網路安全群組關聯/取消關聯至網路介面
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。 第二個命令會取得一個名為 MyNSG 的現有網路安全性群組，並將它儲存在 $nsg 變數中。 第三個命令會將 $nsg 指派給 $nic。 最後，第四個命令會將變更套用至網路介面。 若要將網路安全群組與網路介面取消關聯，請在第三個命令中使用 $null 簡單地取代 $nsg。

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

### -NetworkInterface
指定代表要設定網路介面之狀態的網路介面物件。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
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

### PSNetworkInterface 中的 [.]

## 輸出

### PSNetworkInterface 中的 [.]

## 筆記

## 相關連結

[AzNetworkInterface](./Get-AzNetworkInterface.md)

[AzNetworkInterface](./Get-AzNetworkInterface.md)

[新-AzNetworkInterface](./New-AzNetworkInterface.md)

[移除-AzNetworkInterface](./Remove-AzNetworkInterface.md)
