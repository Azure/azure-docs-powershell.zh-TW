---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 260cf95d04d6a923acbdeaa91a412aa0046d9ea0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901774"
---
# Get-AzNotificationHubAuthorizationRule

## 簡介
獲得與通知中樞相關聯的授權規則相關資訊。

## 語法

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzNotificationHubAuthorizationRule** Cmdlet 會取得與通知中樞相關聯的共用存取簽章 (SAS) 授權規則相關資訊。
Cmdlet 會返回與中樞相關聯的所有規則相關資訊，或包含 *AuthorizationRule* 參數，以獲得特定規則的資訊。
授權規則可管理您通知中樞的存取權。
授權規則會根據不同的許可權等級，建立連結作為 URI。
用戶端會依據適當的許可權等級，導向至其中一個 URI。
例如，具有聆聽許可權的用戶端會導向至該許可權的 URI。
**Get-AzNotificationHubAuthorizationRule** Cmdlet 只會取得與通知中樞相關聯的授權規則相關資訊。
若要取得中樞本身的資訊，請使用 Get-AzNotificationHub。

## 例子

### 範例 1：取得指派給通知中心之所有授權規則的資訊
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

此命令會針對指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞的所有授權規則，獲得相關資訊。
您必須指定中樞所在的命名空間，以及中樞已指派給的資源群組。

### 範例 2：取得指派給通知中樞之授權規則的資訊
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

此命令會針對指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞的所有授權規則，獲得相關資訊。
該命令使用 *AuthorizationRule* 參數，將所返回的資料限制為名為 ListenRule 的單一授權規則。

## 參數

### -AuthorizationRule
指定 SAS 驗證規則的名稱。
這些規則會決定使用者對通知中樞的存取類型。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
指定此 Cmdlet 指派授權規則的通知中樞。
通知中樞可用來傳送推入通知給多個用戶端，無論這些用戶端使用哪個平臺。

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
指定指派通知中樞給的資源群組。
資源群組會以有助於簡化庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes

## 筆記

## 相關連結

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


