---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448746"
---
# New-AzureRmVmssIpConfig

## 摘要
為 VMSS 的網路介面建立 IP 配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmVmssIpConfig** Cmdlet 會為虛擬機器縮放集 (VMSS) 的網路介面建立 IP 設定物件。
將此 Cmdlet 的配置指定為 Add-AzureRmVmssNetworkInterfaceConfiguration Cmdlet 的 *IPConfiguration* 參數。

## 示例

### 範例1：建立 VMSS 介面的 IP 設定物件
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

這個命令會建立名為 ContosoVmssInterface02 的 IP 設定物件。
此命令會使用 $SubnetId 中儲存的先前定義子網 ID。
此命令會將設定設定儲存在 $IPConfiguration 變數中，以便日後與 **AzureRmVmssNetworkInterfaceConfiguration** 搭配使用。

### 範例2：建立包含 NAT 池設定的 IP 設定物件
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

這個命令會建立名為 ContosoVmssInterface03 的 IP 設定物件，然後將它儲存在 $IPConfiguration 變數中供日後使用。
此命令會使用 $SubnetId 中儲存的先前定義子網 ID。
該命令會將設定設定儲存在 $IPConfiguration 變數中，以供日後使用。
此命令會指定 *LoadBalancerInboundNatPoolsId* 和 *LoadBalancerBackendAddressPoolsId* 參數的值。

## 參數

### -ApplicationGatewayBackendAddressPoolsId
指定 [負載平衡器] 後端位址集區的參照陣列。
比例集可以參照一個公用與一個內部負載平衡器的後端位址集區。
多個規模集不能使用相同的負載平衡器。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsSetting
要套用於 publicIP 位址的 dns 設定。
要套用於 publicIP 位址的 Dns 設定的功能變數名稱標籤。
網功能變數名稱稱標籤和 vm 索引的串聯將是將要建立之公用 IP 位址資源的功能變數名稱標籤。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -識別碼
指定 ID。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
指定在負載平衡器) 池的傳入網路位址轉譯 (NAT 的參照陣列。
比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。
多個規模集不能使用相同的負載平衡器。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
指定到負載平衡器內傳的 NAT 池的參照陣列。
比例集可以參照一個公用與一個內部負載平衡器的傳入 NAT 池。
多個規模集不能使用相同的負載平衡器。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定 IP 配置的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
指定 ip 配置是 IPv4 或 IPv6。 預設值會做為 IPv4。  可能的值為： "IPv4" 和 "IPv6"。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
公用 IP 位址的空閒超時。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
[PublicIP 位址] 配置名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
指定設定在其中建立 VMSS 網路介面的子網 ID。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[附加 AzureRmVmssNetworkInterfaceConfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


