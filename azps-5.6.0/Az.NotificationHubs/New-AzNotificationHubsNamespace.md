---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 20a4da67030962a238838247a7dcf137208e56b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901737"
---
# New-AzNotificationHubsNamespace

## 簡介
建立通知中樞命名空間。

## 語法

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 描述
**New-AzNotificationHubsNamespace** Cmdlet 會建立通知中樞命名空間。
命名空間是邏輯容器，可協助組織及管理通知中樞。
您至少必須有一個通知中樞命名空間。
單一命名空間可以包含多個中樞。
您可以有多個命名空間來組織中樞，或將管理所選中樞子集的許可權授予特定人員。
若要建立命名空間，請確定您為命名空間指定唯一名稱;指定命名空間所在的資料中心;，然後指定要指派命名空間的資源群組。
建立命名空間之後，您可以使用 New-AzNotificationHubsNamespaceAuthorizationRules Cmdlet 將授權規則指派給該命名空間。
授權規則可用來管理命名空間的許可權。

## 例子

### 範例 1：建立通知中樞
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

此命令會建立名為 ContosoPartners 的通知中樞。
命名空間將位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。

### 範例 2：建立包含標記的通知中樞
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

此命令會建立名為 ContosoPartners 的通知中樞。
命名空間將位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。
此外，此命令會建立一個標記，其名稱為物件和 PartnerOrganizations 值，並指派給命名空間。
這可確保每次篩選物件標記設定為 PartnerOrganizations 的專案時，都會顯示命名空間。

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

### -位置
指定將託管命名空間之資料中心的顯示名稱。
雖然您可以將此參數設定為任何有效的位置，但為了獲得最佳的績效，您可能會想要使用靠近大多數使用者的資料中心。

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

### -命名空間
指定新命名空間的名稱。
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
指定要指派命名空間的資源群組。
資源群組會以只協助庫存管理和管理的方式整理專案，例如命名空間、通知中樞和授權規則。

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

### -SkuTier
命名空間的 SKU 層級

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -標記
指定可用來分類及組織 Azure 專案的名稱值組。
標記的運作方式類似關鍵字，而且可在整個部署中運作。
例如，如果您搜尋具有標記部門：IT 的所有專案，無論專案類型、位置或資源群組，搜尋都會返回所有具有該標記的 Azure 專案。
個別標記由兩個部分組成： *名稱* ，以及值 ，或者，選擇性地 *是值*。
例如，在部門：IT 中，標記名稱為部門，而標記值為 IT。
若要新增標記，請使用類似此的雜湊表格語法，這會建立標記 CalendarYear：2016：

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。 不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes

## 筆記

## 相關連結

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


