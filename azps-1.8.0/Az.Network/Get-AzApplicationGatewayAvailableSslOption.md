---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622114"
---
# Get-AzApplicationGatewayAvailableSslOption

## 摘要
取得適用于應用程式閘道之 ssl 原則的所有可用 ssl 選項。

## 句法

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzApplicationGatewayAvailableSslOption** Cmdlet 會取得 ssl 原則的所有可用 ssl 選項

## 示例

### 範例1
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

這個命令會傳回 ssl 原則的所有可用 ssl 選項。

## 參數

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### PSApplicationGatewayAvailableSslOptions 中的 [.]

## 筆記

## 相關連結
