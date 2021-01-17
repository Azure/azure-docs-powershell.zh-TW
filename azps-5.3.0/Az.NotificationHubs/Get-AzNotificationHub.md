---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448828"
---
# Get-AzNotificationHub

## 摘要
取得通知中樞的相關資訊。

## 句法

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzNotificationHub** Cmdlet 會取得指定命名空間中的通知中心相關資訊，並指派給指定的資源群組。
例如，您可以取得命名空間 ContosoNamespace 中所有通知中心的資訊，並指派給 ContosoNotificationsGroup 資源群組。
或者，您也可以使用 *NotificationHub* 參數，將傳回的資料限制為特定通知中樞的相關資訊。
通知中樞是用來傳送推播通知給多個用戶端，而不論平臺為何（例如 iOS、Android、Windows Phone 8 和 Windows Store）都是由這些用戶端所使用。
這些中樞大致相當於個別應用程式，而您的每個應用程式通常都有自己的通知中樞。
這個 Cmdlet 只會取得中心本身的相關資訊。
您需要使用其他 Cmdlet （例如 AzNotificationHubAuthorizationRules、AzNotificationHubListKeys 和 AzNotificationHubPNSCredentials）來取得中樞的授權規則、連接字串及平臺通知服務認證的相關資訊。

## 示例

### 範例1：取得特定命名空間中所有通知中心的相關資訊
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

這個命令會取得名為 ContosoNamespace 的命名空間中已指派給資源群組 ContosoNotificationsGroup 的所有通知中心的資訊。

### 範例2

取得通知中樞的相關資訊。  (自動生成) 

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定此 Cmdlet 所取得之通知中樞的名稱。
通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### NotificationHubAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[AzNotificationHubListKey](./Get-AzNotificationHubListKey.md)

[AzNotificationHubPNSCredential](./Get-AzNotificationHubPNSCredential.md)

[新-AzNotificationHub](./New-AzNotificationHub.md)

[移除-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


