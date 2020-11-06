---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449058"
---
# Get-AzureRmApplicationGatewayHttpListenerCustomError

## 摘要
從應用程式閘道的 HTTP 攔截器) 取得自訂錯誤 (s。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
AzureRmApplicationGatewayCustomError Cmdlet 會從應用程式閘道的 HTTP 攔截器) ， **取得** 自訂錯誤 (s。

## 示例

### 範例1：在 HTTP 偵聽程式中取得自訂錯誤
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

這個命令會從 HTTP 偵聽程式 $listener 01 中取得並傳回 HTTP 狀態碼502的自訂錯誤。

### 範例2：取得 HTTP 偵聽程式中所有自訂錯誤的清單
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

這個命令會從 HTTP 偵聽程式 $listener 01 中取得並傳回所有自訂錯誤的清單。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -HttpListener
應用程式閘道 Http 攔截器

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
應用程式閘道客戶錯誤的狀態碼。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。
如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSApplicationGatewayHttpListener 中的 [.]

## 輸出

### PSApplicationGatewayCustomError 中的 [.]

## 筆記

## 相關連結
