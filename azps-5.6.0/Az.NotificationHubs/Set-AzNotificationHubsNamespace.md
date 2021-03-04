---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 7535ff45b8350cb107b7593dc78ab0709d747f8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901701"
---
# Set-AzNotificationHubsNamespace

## 簡介
設定通知中樞命名空間的屬性值。

## 語法

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Set-AzNotificationHubsNamespace** Cmdlet 會設定現有通知中樞命名空間的屬性值。
命名空間是邏輯容器，可協助組織及管理通知中樞。
您至少必須有一個通知中樞命名空間。
此外，所有通知中樞都必須有指派的命名空間。
此 Cmdlet 主要用來啟用和停用命名空間。
當命名空間停用時，使用者無法連接到命名空間中任何通知中樞，系統管理員也無法使用這些中樞來傳送推入通知。
若要重新啟用停用的命名空間，請使用此 Cmdlet 將 **命名空間的 State** 屬性設為 Active。
您也可以使用此 Cmdlet 將命名空間標記為重要。
這可防止命名空間遭到刪除。
若要移除重要命名空間，您必須先移除重要標記。

## 例子

### 範例 1：停用命名空間
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

此命令會停用名稱為 ContosoPartners 的命名空間，該命名空間位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。

### 範例 2：啟用命名空間
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

此命令啟用名稱為 ContosoPartners 的命名空間，位於美國西部資料中心，並指派給 ContosoNotificationsGroup 資源群組。

## 參數

### -重要
指出命名空間是否是重要的命名空間。
無法刪除重要命名空間。
若要刪除重要命名空間，您必須將此屬性的值設為 False，才能將命名空間標記為非重要。

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

### -強制
請勿要求確認。

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
指定託管命名空間之資料中心的顯示名稱。
雖然您可以將此參數設定為任何有效的 Azure 位置，但為了獲得最佳的績效，您應該使用靠近大多數使用者的資料中心。
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
指定指派命名空間的資源群組。
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

### -State
指定命名空間的目前狀態。
此參數可接受的值為：使用中和已停用。

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

### -標記
指定可用來分類及組織 Azure 專案的名稱值組。
標記的運作方式類似關鍵字，而且可在整個部署中運作。
例如，如果您搜尋具有標記部門：IT 的所有專案，無論專案類型、位置或資源群組，搜尋都會返回所有具有該標記的 Azure 專案。
個別標記包含兩個部分：名稱 (選擇性地) *值*。
例如，在 Department：IT 中，標記名稱為部門，而標記值為 IT。
若要新增標記，請使用類似此的雜湊表格語法，這會建立標記 CalendarYear：2016：-Tag @{Name="CalendarYear";Value="2016"} 若要在同一個命令中新增多個標記，請以逗號分隔個別標記：-Tag @{Name="CalendarYear";Value="2016"}， @{Name="FiscalYear";Value="2017"}

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

### Microsoft.Azure.Commands.NotificationHubs.models.命名空間狀態

### System.Boolean

### System.Collections.Hashtable

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes

## 筆記

## 相關連結

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


