---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910966"
---
# Set-AzNetworkInterface

## 簡介
更新網路介面。

## 語法

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Set-AzNetworkInterface 會** 更新網路介面。

## 例子

### 範例 1：設定網路介面
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

此範例會設定網路介面。
第一個命令會獲得資源群組 ResourceGroup1 中名為 NetworkInterface1 的網路介面。
第二個命令會設定 IP 設定的私人 IP 位址。
第三個命令將私人 IP 分配方法設定為靜態。
第四個命令會設定網路介面上的標記。
第五個命令使用儲存在 $Nic 變數的資訊來設定網路介面。

### 範例 2：變更網路介面上的 DNS 設定
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

第一個命令會獲得名稱為 NetworkInterface1 的網路介面，該介面存在於資源群組 ResourceGroup1 中。 第二個命令會將 DNS 伺服器 192.168.1.100 新增到此介面。 第三個命令會將這些變更適用于網路介面。 若要移除 DNS 伺服器，請遵循上述命令，但取代 "。新增" 加上 "。第二個命令中的移除」。

### 範例 3：在網路介面上啟用 IP 轉轉
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

第一個命令會獲得稱為 NetworkInterface1 的現有網路介面，並儲存在$nic變數。 第二個命令將 IP 轉轉值變更為 True。 最後，第三個命令將變更適用于網路介面。 若要停用網路介面上的 IP 轉轉，請遵循範例範例，但請務必將第二個命令變更為「$nic。EnableIPForwarding = 0"。

### 範例 4：變更網路介面的子網
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

第一個命令會獲得網路介面 NetworkInterface1，並儲存在$nic變數。 第二個命令會獲得與網路介面將要關聯的子網相關聯的虛擬網路。 第二個命令會獲得子網，並儲存在 $subnet 2 變數中。 第三個命令會關聯網路介面的主要私人 IP 位址與新的子網。 最後，最後一個命令將這些變更應用在網路介面上。
>[!NOTE] 
>IP 組配置必須是動態的，您才能變更子網。 如果您有靜態 IP 組案，請變更為動態，再繼續進行。 
>[!NOTE]
>如果網路介面有多個 IP 組配置，則必須針對所有這些 IP 組配置執行第四個命令，才能執行Set-AzNetworkInterface命令。 這可以在第四個命令中執行，但以適當的數位取代 "0"。 如果網路介面有 N IP 組式，則這些命令的 N-1 必須存在。

### 範例 5：將網路安全性群組關聯/解除關聯至網路介面
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

第一個命令會獲得稱為 NetworkInterface1 的現有網路介面，並儲存在$nic變數。 第二個命令會獲得名為 MyNSG 的現有網路安全性群組，並儲存在 $nsg 變數中。 第三個命令會$nsg指派$nic。 最後，第四個命令將變更適用于網路介面。 若要將網路安全性群組與網路介面解除關聯，請以 $nsg 取代第三個命令$null。

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

### -NetworkInterface
指定代表網路介面應設定之狀態的網路介面物件。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.Network.models.PSNetworkInterface

## 輸出

### Microsoft.Azure.Commands.Network.models.PSNetworkInterface

## 筆記

## 相關連結

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
