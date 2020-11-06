---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 284e283eb05608524e0a746a2b5eeb1769e368a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621352"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## 摘要
取得與通知中心命名空間相關聯之授權規則的相關資訊。

## 句法

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會傳回有關共用存取簽章 (SAS) 與通知中心命名空間相關聯的授權規則的資訊。
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
若要取得命名空間本身的相關資訊，請使用 AzNotificationHubsNamespace。

## 示例

### 範例1：取得指派給命名空間的所有授權規則的相關資訊
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

這個命令會取得指派給 namespace ContosoNamespace 和 ContosoNotificationsGroup 資源群組的所有授權規則的相關資訊。

### 範例2：取得授權規則的相關資訊
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
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

[AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[新-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[移除-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


