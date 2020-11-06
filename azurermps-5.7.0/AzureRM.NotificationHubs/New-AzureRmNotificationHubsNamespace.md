---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 504fe8b5aad0e2e028bf27cf08a29fd335edfa33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449258"
---
# New-AzureRmNotificationHubsNamespace

## 摘要
建立通知中心命名空間。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmNotificationHubsNamespace** Cmdlet 會建立通知中心命名空間。

命名空間是邏輯容器，可協助您組織和管理通知中樞。
您至少必須有一個通知中樞命名空間。
單一命名空間可以存放多個中心。
您可以有多個命名空間來組織您的中樞，或提供特定的個人許可權來管理您的中樞的選取子集。

若要建立命名空間，請確定您指定的是命名空間的唯一名稱;指定命名空間所在的資料中心;然後，指定要將命名空間指派給哪個資源群組。
在命名空間建立之後，您可以使用 New-AzureRmNotificationHubsNamespaceAuthorizationRules Cmdlet 來將授權規則指派給該命名空間。
授權規則是用來管理命名空間的許可權。

## 示例

### 範例1：建立通知中樞
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

這個命令會建立名為 ContosoPartners 的通知中樞。
該命名空間會位於 [西部美國資料中心]，並指派給 ContosoNotificationsGroup 資源群組。

### 範例2：使用標記建立通知中樞
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

這個命令會建立名為 ContosoPartners 的通知中樞。
該命名空間會位於 [西部美國資料中心]，並指派給 ContosoNotificationsGroup 資源群組。
此外，這個命令會建立一個含有名稱物件和值 PartnerOrganizations 的標記，並指派給命名空間。
這可確保您在每次篩選物件都設定為 PartnerOrganizations 的專案時，都會顯示該命名空間。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -位置
指定將主控命名空間的資料中心的顯示名稱。
雖然您可以將此參數設定為任何有效的位置，但若要獲得最佳效能，您可能會想要使用靠近使用者的資料中心。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -命名空間
指定新命名空間的名稱。
命名空間提供一種群組和分類通知中樞的方式。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
指定要將命名空間指派給哪個資源群組。
資源群組會以協助您輕鬆清點管理和管理的方式來組織諸如命名空間、通知中樞和授權規則等專案。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
命名空間的 Sku 層級

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
指定可用於分類及組織 Azure 專案的名稱-值對。
標記的功能與關鍵字類似，且可在整個部署中運作。
例如，如果您在所有專案中搜尋標籤部：這項搜尋將會傳回所有具有該標記的 Azure 專案，不論專案類型、位置或資源群組為何。

個別標籤由兩個部分組成： *名稱* 與（可選擇） *值* 。
例如，在 [部門] 中，標記名稱是 [部門]，而標記值是 [部門]。
若要新增標籤，請使用類似這個的雜湊資料表語法，這會建立 tag CalendarYear：2016：

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### NamespaceAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[移除-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


