---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449053"
---
# Get-AzureRmLoadBalancerBackendAddressPoolConfig

## 摘要
取得負載平衡器的後端位址集區配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會取得單一後端位址集區或負載平衡器內後端位址集區清單。

## 示例

### 範例1：取得後端位址集區
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

第一個命令會在名為 MyResourceGroup 的資源群組中，取得名為 MyLoadBalancer 的現有負載平衡器，然後將它儲存在 $loadbalancer 變數中。
第二個命令會針對 $loadbalancer 中的負載平衡器，取得名為 BackendAddressPool02 的關聯後端位址集區配置。

## 參數

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

### -LoadBalancer
指定與要取得的後端位址集區相關聯的負載平衡器。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -名稱
指定包含要取得之後端位址集區的負載平衡器名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSLoadBalancer 中的 [.]
參數： LoadBalancer (ByValue) 

## 輸出

### PSBackendAddressPool 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmLoadBalancerBackendAddressPoolConfig](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[新-AzureRmLoadBalancerBackendAddressPoolConfig](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[移除-AzureRmLoadBalancerBackendAddressPoolConfig](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


