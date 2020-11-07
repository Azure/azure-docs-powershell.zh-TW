---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 978db7296b9789f738f5b277a4bf3731803fdcd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801957"
---
# Set-AzureRmNetworkInterface

## 摘要
設定網路介面的目標狀態。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNetworkInterface 設定** 的是 Azure network 介面的目標狀態。

## 示例

### 範例1：設定網路介面
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

這個範例會設定網路介面。
第一個命令會在資源群組 ResourceGroup1 中取得名為 NetworkInterface1 的網路介面。
第二個命令會設定 IP 配置的私人 IP 位址。
第三個命令會將專用 IP 配置方法設定為 Static。
第四個命令會在網路介面上設定標記。
第五個命令使用儲存在 $Nic 變數中的資訊來設定網路介面。

### 範例2：變更網路介面上的 DNS 設定
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的網路介面，該網路介面存在於資源群組 ResourceGroup1 中。 第二個命令會將 DNS 伺服器192.168.1.100 新增到這個介面。 第三個命令會將這些變更套用至網路介面。 若要移除 DNS 伺服器，請遵循上面所列的命令，但要取代 "。新增 "with"。第二個命令中的 [移除]。

### 範例3：在網路介面上啟用 IP forwading
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。 第二個命令會將 IP 轉寄值變更為 true。 最後，第三個命令會將變更套用至網路介面。 若要在網路介面上停用 IP 轉寄功能，請遵循範例範例，但務必將第二個命令改為「$nic。EnableIPForwarding = 0 "。

### 範例4：變更網路介面的子網
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

第一個命令會取得網路介面 NetworkInterface1，並將它儲存在 $nic 變數中。 第二個命令會取得與網路介面將要關聯之子網相關聯的虛擬網路。 第二個命令會取得子網，並將它儲存在 $subnet 2 變數中。 第三個命令會將網路介面的主要私人 IP 位址與新的子網相關聯。 最後，最後一個命令會在網路介面上套用這些變更。

>[!NOTE] 
>您必須先動態使用 IP 設定，才能變更子網。 如果您有靜態 IP 設定，請先將它變更為 [動態]，然後再繼續進行。 

>[!NOTE]
>如果網路介面有多個 IP 設定，則在執行最後一個 Set-AzureRmNetworkInterface 命令之前，必須完成所有這些 IP 設定的第四個命令。 您可以在第四個命令中完成，但將 "0" 取代為適當的數位。 如果網路介面具有 N 個 IP 配置，則必須存在這些命令的 N-1。

### 範例5：將網路安全群組關聯/取消關聯至網路介面
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

第一個命令會取得名為 NetworkInterface1 的現有網路介面，並將它儲存在 $nic 變數中。 第二個命令會取得一個名為 MyNSG 的現有網路安全性群組，並將它儲存在 $nsg 變數中。 第四個命令會將 $nsg 指派給 $nic。 最後，第五個命令會將變更套用至網路介面。 若要將網路安全群組與網路介面取消關聯，請在第四個命令中簡單地取代 $nsg $null。

## 參數

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: SwitchParameter
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterface
指定代表網路介面目標狀態的 **NetworkInterface** 物件。

```yaml
Type: PSNetworkInterface
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

### PSNetworkInterface
形參 "NetworkInterface" 接受管線中 "PSNetworkInterface" 類型的值

## 輸出

### PSNetworkInterface 中的 [.]

## 筆記

## 相關連結

[AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[AzureRmNetworkInterface](./Get-AzureRmNetworkInterface.md)

[新-AzureRmNetworkInterface](./New-AzureRmNetworkInterface.md)

[移除-AzureRmNetworkInterface](./Remove-AzureRmNetworkInterface.md)
