---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e0131701764fd912e5583bae6add3e43265faade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447769"
---
# Remove-AzureRmLoadBalancerBackendAddressPoolConfig

## 摘要
從負載平衡器移除後端位址集區配置。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmLoadBalancerBackendAddressPoolConfig** Cmdlet 會從負載平衡器中移除後端位址集區。

## 示例

### 範例1：從負載平衡器移除後端位址集區設定
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

這個命令會取得名為 MyLoadBalancer 的負載平衡器，並將它傳遞給 **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** ，這會從 MyLoadBalancer 中移除 BackendAddressPool02 設定。
最後，Set-AzureRmLoadBalancer Cmdlet 更新 MyLoadBalancer。
請注意，後端位址集區配置必須存在，才能刪除。

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

### -LoadBalancer
指定包含要移除之後端位址集區的負載平衡器。

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 移除之後端位址集區的名稱。

```yaml
Type: String
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

### PSLoadBalancer
形參 "LoadBalancer" 接受管線中 "PSLoadBalancer" 類型的值

## 輸出

### PSLoadBalancer 中的 [.]

## 筆記

## 相關連結

[附加 AzureRmLoadBalancerBackendAddressPoolConfig](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[AzureRmLoadBalancer](./Get-AzureRmLoadBalancer.md)

[AzureRmLoadBalancerBackendAddressPoolConfig](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[新-AzureRmLoadBalancerBackendAddressPoolConfig](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


