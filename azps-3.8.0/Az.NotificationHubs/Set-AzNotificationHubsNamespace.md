---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958705"
---
# Set-AzNotificationHubsNamespace

## 摘要
設定通知中心命名空間的屬性值。

## 句法

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzNotificationHubsNamespace** Cmdlet 會設定現有通知中心命名空間的屬性值。
命名空間是邏輯容器，可協助您組織和管理通知中樞。
您至少必須有一個通知中樞命名空間。
此外，所有通知中樞都必須有指派的命名空間。
這個 Cmdlet 主要是用來啟用和停用命名空間。
當命名空間停用時，使用者無法連線到命名空間中的任何通知中樞，也不能使用這些中樞傳送推播通知。
若要重新啟用停用的命名空間，請使用此 Cmdlet 將命名空間的 **State** 屬性設定為 [作用中]。
您也可以使用此 Cmdlet 將命名空間標記為重要。
這可防止刪除命名空間。
若要移除重要的命名空間，您必須先移除 [重要] 標籤。

## 示例

### 範例1：停用命名空間
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

這個命令會停用位於 [美國西部] 資料中心並指派給 ContosoNotificationsGroup 資源群組的命名空間 ContosoPartners。

### 範例2：啟用命名空間
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

這個命令會啟用位於西部美國資料中心並指派給 ContosoNotificationsGroup 資源群組的命名空間 ContosoPartners。

## 參數

### -重要
指出命名空間是否為關鍵命名空間。
無法刪除關鍵命名空間。
若要刪除關鍵命名空間，您必須將此屬性的值設為 False，才能將命名空間標示為非重要。

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -Force
不要要求確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
指定承載命名空間的資料中心的顯示名稱。
雖然您可以將此參數設定為任何有效的 Azure 位置，但若要獲得最佳效能，您應該使用接近大多數使用者的資料中心。
若要取得最新的 Azure 位置清單，請執行下列命令： `Get-AzLocation | Select-Object DisplayName`

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
指定此 Cmdlet 修改的命名空間。
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
指定將命名空間指派給哪個資源群組。
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

### -SkuTier
命名空間的 Sku 層級

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

### -State
指定命名空間的目前狀態。
此參數可接受的值為： [作用中] 和 [已停用]。

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
指定可用於分類及組織 Azure 專案的名稱-值對。
標記的功能與關鍵字類似，且可在整個部署中運作。
例如，如果您在所有專案中搜尋標籤部：這項搜尋將會傳回所有具有該標記的 Azure 專案，不論專案類型、位置或資源群組為何。
個別標記由兩個部分組成： [ *名稱* ] 和 [ (] 可選擇) *值* 。
例如，在 [部門]： IT 中，標籤名稱是 [部門]，而 tag 值則是。
若要新增標籤，請使用類似這個的雜湊表語法，這會建立標記 CalendarYear：2016：-Tags @ {Name = "CalendarYear";值 = "2016"} 若要在相同的命令中新增多個標籤，請使用逗號分隔個別的標記：-Tag @ {Name = "CalendarYear";值 = "2016"}，@ {Name = "FiscalYear";Value = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### NamespaceState 中的 NotificationHubs。

### System.object

### [System.object] 集合. Hashtable

## 輸出

### NamespaceAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[新-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[移除-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


