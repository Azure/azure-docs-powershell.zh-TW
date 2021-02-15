---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400615"
---
# Get-AzNotificationHub

## 簡介
獲得有關通知中樞的資訊。

## 語法

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzNotificationHub** Cmdlet 會取得指定命名空間中通知中樞的資訊，並指派給指定的資源群組。
例如，您可以取得命名空間 ContosoNamespace 中所有通知中樞的資訊，並指派給 ContosoNotificationsGroup 資源群組。
或者，您可以使用 *NotificationHub* 參數，將所返回的資料限制為特定通知中樞的資訊。
通知中樞可用來傳送推入通知給多個用戶端，而不管這些用戶端所使用的平臺是 iOS、Android、Windows Phone 8 和 Windows 市集。
這些中樞大致相當於個別的應用程式，而且每一個 App 通常會有自己的通知中樞。
此 Cmdlet 只會獲得中樞本身的資訊。
其他 Cmdlet ，例如 Get-AzNotificationHubAuthorizationRules、Get-AzNotificationHubListKeys 和 Get-AzNotificationHubPNSCredentials，都需要取得中樞的授權規則、連接字串和平臺通知服務認證相關資訊。

## 例子

### 範例 1：取得特定命名空間中所有通知中樞的資訊
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

此命令會獲得名稱為 ContosoNamespace 之命名空間中所有已指派給資源群組 ContosoNotificationsGroup 的通知中樞資訊。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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
指定指派通知中樞的命名空間。
命名空間提供將通知中樞分組和分類的方式。

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
指定此 Cmdlet 獲得的通知中樞名稱。
通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。

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
指定指派通知中樞給的資源群組。
資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.NotificationHubAttributes

## 筆記

## 相關連結




[New-AzNotificationHub](./New-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


