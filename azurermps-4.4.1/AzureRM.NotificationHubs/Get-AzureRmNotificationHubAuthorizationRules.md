---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456468"
---
# Get-AzureRmNotificationHubAuthorizationRules

## 摘要
取得與通知中樞相關聯之授權規則的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubAuthorizationRules** Cmdlet 會取得共用存取簽章 (SAS) 與通知中樞相關聯的授權規則的資訊。
Cmdlet 會傳回與中心有關的所有規則的相關資訊，或包含 *AuthorizationRule* 參數，取得特定規則的相關資訊。

授權規則可管理您通知中樞的存取權。
授權規則將根據不同的許可權等級，以 URI 來建立連結。
用戶端會根據適當的許可權等級，導向到其中一個 Uri。
例如，擁有 [偵聽] 許可權的客戶將會被導向該許可權的 URI。

**AzureRmNotificationHubAuthorizationRules** Cmdlet 只會取得與通知中樞相關聯之授權規則的相關資訊。
若要取得中心本身的相關資訊，請使用 AzureRmNotificationHub。

## 示例

### 範例1：取得指派給通知中心的所有授權規則資訊
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。
您必須指定中樞所在的命名空間，以及該中樞已獲指派的資源群組。

### 範例2：取得指派給通知中心的授權規則資訊
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

這個命令會取得指派給命名空間 ContosoNamespace 中名為 ContosoInternalHub 之通知中樞之所有授權規則的資訊。
此命令會使用 *AuthorizationRule* 參數，將傳回的資料限制為單一的名為 ListenRule 的授權規則。

## 參數

### -AuthorizationRule
指定 SAS 驗證規則的名稱。
這些規則決定使用者對通知中樞所擁有的存取類型。

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
指定此 Cmdlet 指派授權規則的通知中樞。
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
資源群組會以協助簡化庫存管理和 Azure 管理的方式，來組織諸如命名空間、通知中心及授權規則等專案。

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

### [System.object]. 清單 ' 1 [NotificationHubs]。 SharedAccessAuthorizationRuleAttributes]

## 筆記

## 相關連結

[AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[新-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[移除-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


