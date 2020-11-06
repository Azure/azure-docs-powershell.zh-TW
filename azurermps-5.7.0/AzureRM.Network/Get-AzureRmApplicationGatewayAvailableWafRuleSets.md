---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: fb16474d8a23f528aaaeb498ced4fa5a3e952236
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "93457668"
---
# Get-AzureRmApplicationGatewayAvailableWafRuleSets

## 摘要
取得所有可用的 web 應用程式防火牆規則集。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmApplicationGatewayAvailableWafRuleSets** Cmdlet 會取得所有可用的 web 應用程式防火牆規則集。

## 示例

### 範例1
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

這個命令會傳回所有可用的 web 應用程式防火牆規則集。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSApplicationGatewayAvailableWafRuleSetsResult 中的 [.]

## 筆記
**清單-AzureRmApplicationGatewayAvailableWafRuleSets** 是 **AzureRmApplicationGatewayAvailableWafRuleSets** Cmdlet 的別名。

## 相關連結

