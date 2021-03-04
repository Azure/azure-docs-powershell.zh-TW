---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915365"
---
# Get-AzApplicationGatewayAvailableSslOption

## 簡介
針對應用程式閘道的 ssl 策略，獲得所有可用的 ssl 選項。

## 語法

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzApplicationGatewayAvailableSlOption** Cmdlet 會取得 ssl 政策的所有可用 ssl 選項

## 例子

### 範例 1
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

這個命令會針對 ssl 策略，會返回所有可用的 ssl 選項。

## 參數

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAvailableSlOptions

## 筆記

## 相關連結
