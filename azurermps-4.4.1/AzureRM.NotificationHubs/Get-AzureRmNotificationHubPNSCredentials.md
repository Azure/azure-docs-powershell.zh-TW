---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 2CCDF339-9D6E-4B0C-9201-BE641C8827F6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubPNSCredentials.md
ms.openlocfilehash: 29f4871b6299685ae5791f82498083956a7e4048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448092"
---
# Get-AzureRmNotificationHubPNSCredentials

## 摘要
取得通知中樞的 PNS 認證。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmNotificationHubPNSCredentials [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubPNSCredentials** Cmdlet 會取得平臺通知服務， () PNS 通知中樞的認證。
每個通知中樞都有一組 PNS 認證。
這些認證會套用到個別的推播通知服務，例如但不限於;iOS 推播通知服務、Android 推播通知服務和 Windows Phone 8。

## 示例

### 範例1：取得特定通知中樞的 PNS 認證
```
PS C:\>Get-AzureRmNotificationHubPNSCredentials -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

這個命令會取得名為 ContosoInternalHub 的通知中樞的 PNS 認證，該通知中心屬於名為 ContosoNotificationsGroup 的資源群組。

## 參數

### -命名空間
指定通知中心指派給哪個命名空間。

命名空間提供一種群組和分類通知中樞的方式。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
指定指派 PNS 認證的通知中樞。

通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
指定通知中心指派給哪個資源群組。

資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### NotificationHubAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHub](./Get-AzureRmNotificationHub.md)


