---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452803"
---
# Get-AzureRmApplicationGatewayProbeConfig

## 摘要
從應用程式閘道取得現有的健康情況探測設定。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
Get-AzureRmApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道取得現有的健康情況探測設定。

## 示例

### 範例1：從應用程式閘道取得現有的探測
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

這個命令會從名為「閘道」的應用程式閘道取得名為 Probe02 的 health 探測。

## 參數

### -ApplicationGateway
指定此 Cmdlet 取得探測設定的應用程式閘道。

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -名稱
指定探測器的名稱。

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

### PSApplicationGateway 中的 [.]
參數： ApplicationGateway (ByValue) 

## 輸出

### PSApplicationGatewayProbe 中的 [.]

## 筆記

## 相關連結

[新增探測至現有的應用程式閘道](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[附加 AzureRmApplicationGatewayProbeConfig]()

[新-AzureRmApplicationGatewayProbeConfig]()

[移除-AzureRmApplicationGatewayProbeConfig]()

[Set-AzureRmApplicationGatewayProbeConfig]()

