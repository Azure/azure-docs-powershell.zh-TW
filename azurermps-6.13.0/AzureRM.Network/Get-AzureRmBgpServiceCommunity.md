---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermbgpservicecommunity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmBgpServiceCommunity.md
ms.openlocfilehash: f951aab0ab655d073c830d08e2665533c961960a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452779"
---
# Get-AzureRmBgpServiceCommunity

## 摘要
提供所有服務/地區、BGP 社區及相關聯的首碼的清單。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmBgpServiceCommunity [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
這個 Cmdlet 提供所有服務/地區、BGP 社區及相關聯的首碼的清單。

## 示例

### 範例1
```
Get-AzureRmBgpServiceCommunity

...

Name           : AzureCentralIndia
Id             : /subscriptions//resourceGroups//providers/Microsoft.Network/bgpServiceCommunities/AzureCentralIndia
Type           : Microsoft.Network/bgpServiceCommunities
BgpCommunities : [
                   {
                     "ServiceSupportedRegion": "Global",
                     "CommunityName": "Azure Central India",
                     "CommunityValue": "12076:51017",
                     "CommunityPrefixes": [
                       "13.71.0.0/18",
                       "20.190.146.0/25",
                       "40.79.214.0/24",
                       "40.81.224.0/19",
                       "40.87.224.0/22",
                       "40.112.39.0/25",
                       "40.112.39.128/26",
                       "40.126.18.0/25",
                       "52.136.24.0/24",
                       "52.140.64.0/18",
                       "52.159.64.0/19",
                       "52.172.128.0/17",
                       "52.239.135.64/26",
                       "52.239.202.0/24",
                       "52.245.96.0/22",
                       "52.253.168.0/22",
                       "104.47.210.0/23",
                       "104.211.64.0/20",
                       "104.211.81.0/24",
                       "104.211.82.0/23",
                       "104.211.84.0/22",
                       "104.211.88.0/21",
                       "104.211.96.0/19"
                     ],
                     "IsAuthorizedToUse": true,
                     "ServiceGroup": "Azure"
                   }
                 ]
...
```

這個 Cmdlet 提供所有服務/地區、BGP 社區及相關聯的首碼的清單。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSBgpServiceCommunity 中的 [.]

## 筆記

## 相關連結

[移動流覽 AzureRmExpressRouteCircuit](Move-AzureRmExpressRouteCircuit.md)

[新-AzureRmExpressRouteCircuit](New-AzureRmExpressRouteCircuit.md)

[移除-AzureRmExpressRouteCircuit](Remove-AzureRmExpressRouteCircuit.md)

[Set-AzureRmExpressRouteCircuit](Set-AzureRmExpressRouteCircuit.md)

[AzureRmRouteFilter](Get-AzureRmRouteFilter.md)

[AzureRmRouteFilterRuleConfig](Get-AzureRmRouteFilterRuleConfig.md)

[移除-AzureRmRouteFilter](Remove-AzureRmRouteFilter.md)

[移除-AzureRmRouteFilterRuleConfig](Remove-AzureRmRouteFilterRuleConfig.md)

[Set-AzureRmRouteFilter](Set-AzureRmRouteFilter.md)

[Set-AzureRmRouteFilterRuleConfig](Set-AzureRmRouteFilterRuleConfig.md)

[新-AzureRmRouteFilter](New-AzureRmRouteFilter.md)

[新-AzureRmRouteFilterRuleConfig](New-AzureRmRouteFilterRuleConfig.md)
