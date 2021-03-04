---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a1c9743d02f10102d9343709599dbed694d37a2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901746"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## 簡介
與通知中樞命名空間相關聯的授權規則相關資訊。

## 語法

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會返回與通知中樞命名空間相關聯的共用存取簽章 (SAS) 授權規則相關資訊。
您可以返回與命名空間相關聯的所有規則相關資訊。
或者，您也可以包含 *AuthorizationRule* 參數，以返回特定規則的資訊。
授權規則可管理命名空間的存取權。
這是透過根據不同許可權等級建立連結以做為 URI 的方式完成。
平台層級可以是下列其中一個： 
- 聽
- 發送
- 管理用戶端會依據適當的許可權等級，導向至其中一個 URI。
例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。
此 Cmdlet 只會獲得與命名空間相關聯的授權規則。
若要取得命名空間本身的資訊，請使用 Get-AzNotificationHubsNamespace。

## 例子

### 範例 1：取得指派給命名空間之所有授權規則的資訊
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

此命令會獲得指派給命名空間 ContosoNamespace 和 ContosoNotificationsGroup 資源群組之所有授權規則的資訊。

### 範例 2：取得授權規則相關資訊
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

此命令會獲得名為 ListenRule 的單一命名空間授權規則相關資訊。
當您取得特定授權規則的資訊時，必須包含命名空間和資源群組。

## 參數

### -AuthorizationRule
指定 SAS 驗證規則的名稱。
這些規則會決定使用者對於命名空間的存取類型。

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
指定指派授權規則的命名空間。
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

### -ResourceGroup
指定指派授權規則給的資源群組。
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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes

## 筆記

## 相關連結

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


