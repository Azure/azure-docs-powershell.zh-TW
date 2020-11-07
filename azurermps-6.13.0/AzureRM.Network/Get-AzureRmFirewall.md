---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626065"
---
# Get-AzureRmFirewall

## 摘要
取得 Azure 防火牆。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmFirewall** Cmdlet 會取得資源群組中的一個或多個防火牆。

## 示例

### 1：檢索資源群組中的所有防火牆
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

這個範例會檢索資源群組 "rgName" 中的所有防火牆。

### 2：依名稱檢索防火牆
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

這個範例會在資源群組 "rgName" 中，檢索名為 "azFw" 的防火牆。

### 3：檢索防火牆，然後將應用程式規則集合新增到防火牆
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

這個範例會檢索防火牆，然後透過呼叫方法 AddApplicationRuleCollection，將應用程式規則集合新增到防火牆。

### 4：檢索防火牆，然後將網路規則集合新增到防火牆
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

這個範例會檢索防火牆，然後透過呼叫方法 AddNetworkRuleCollection，將網路規則集合新增到防火牆。

### 5：取回防火牆，然後從防火牆以名稱來檢索應用程式規則集合
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

這個範例會檢索防火牆，然後依名稱取得規則集合，並在防火牆物件上呼叫方法 GetApplicationRuleCollectionByName。 方法 GetApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。

### 6：檢索防火牆，然後從防火牆以名稱來檢索網路規則集合
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

這個範例會檢索防火牆，然後依名稱取得規則集合，並在防火牆物件上呼叫方法 GetNetworkRuleCollectionByName。 方法 GetNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。

### 7：從防火牆檢索防火牆，然後依名稱移除應用程式規則集合
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

這個範例會檢索防火牆，然後依名稱移除規則集合，並在防火牆物件上呼叫方法 RemoveApplicationRuleCollectionByName。 方法 RemoveApplicationRuleCollectionByName 的規則集合名稱不區分大小寫。

### 8：檢索防火牆，然後從防火牆移除網路規則集合（依名稱）
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

這個範例會檢索防火牆，然後依名稱移除規則集合，並在防火牆物件上呼叫方法 RemoveNetworkRuleCollectionByName。 方法 RemoveNetworkRuleCollectionByName 的規則集合名稱不區分大小寫。

### 9：取回防火牆，然後再指派防火牆
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

這個範例會在防火牆上檢索防火牆，並在防火牆上進行呼叫，以使用與防火牆相關聯的設定 (應用程式和網路規則集合) 來啟動防火牆服務。

## 參數

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

### -名稱
指定此 Cmdlet 所取得之防火牆的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定防火牆所屬之資源群組的名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### PSAzureFirewall 中的 [.]

## 筆記

## 相關連結

[新-AzureRmFirewall](./New-AzureRmFirewall.md)

[移除-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
