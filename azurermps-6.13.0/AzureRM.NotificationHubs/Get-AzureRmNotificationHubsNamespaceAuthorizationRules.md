---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 9546039459792d5ef72807d8466f728f2060a346
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623912"
---
# Get-AzureRmNotificationHubsNamespaceAuthorizationRules

## 摘要
取得與通知中心命名空間相關聯之授權規則的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubsNamespaceAuthorizationRules** Cmdlet 會傳回有關共用存取簽章 (SAS) 與通知中心命名空間相關聯的授權規則的資訊。
您可以傳回與命名空間關聯的所有規則的相關資訊。
或者，您也可以透過包括 *AuthorizationRule* 參數，傳回特定規則的資訊。
授權規則可管理命名空間的存取權。
這是透過根據不同許可權等級建立連結（例如 Uri）來完成。
平台層級可以是下列其中一項： 
- 聆聽
- 發送
- 系統會根據適當的許可權等級，將管理用戶端導向到其中一個 Uri。
例如，擁有偵聽許可權的用戶端將會導向該許可權的 URI。
這個 Cmdlet 只會取得與命名空間相關聯的授權規則。
若要取得命名空間本身的相關資訊，請使用 AzureRmNotificationHubsNamespace。

## 示例

### 範例1：取得指派給命名空間的所有授權規則的相關資訊
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

這個命令會取得指派給 namespace ContosoNamespace 和 ContosoNotificationsGroup 資源群組的所有授權規則的相關資訊。

### 範例2：取得授權規則的相關資訊
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

這個命令會取得名為 ListenRule 的單一命名空間授權規則的相關資訊。
當您取得特定授權規則的資訊時，您必須包含命名空間和資源群組。

## 參數

### -AuthorizationRule
指定 SAS 驗證規則的名稱。
這些規則決定使用者對命名空間擁有的存取類型。

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
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -命名空間
指定授權規則指派的命名空間。
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

### -ResourceGroup
指定授權規則指派給哪個資源群組。
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[新-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[移除-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


