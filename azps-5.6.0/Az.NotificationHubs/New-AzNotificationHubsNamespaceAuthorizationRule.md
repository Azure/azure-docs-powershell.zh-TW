---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901734"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## 簡介
建立授權規則，並將該規則指派給通知中樞命名空間。

## 語法

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 描述
**New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會建立共用存取簽章 (SAS) 授權規則，並將它指派給通知中樞命名空間。
授權規則會管理命名空間及該命名空間中包含的通知中樞的使用者許可權。
此 Cmdlet 提供兩種方式來建立新授權規則，並將它指派給命名空間。
您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後將該物件設定為您想要新規則擁有的屬性值。
這可以使用 .NET Framework 完成。
接著，您可以使用 *SASRule* 參數，將那些屬性值複製到新規則。
或者，您可以建立 JSON (JavaScript 物件標記法) 包含相關組設定值的檔案，然後使用 *InputFile* 參數來使用這些值。
JSON 檔案是使用類似下列語法的文字檔： {  
    "Name"： "ContosoAuthorizationRule"，  
    "PrimaryKey"："WE4qH0398AyXjlekt56gg1g VM3NHoMs29KkUnnpUk01Y="，  
    "Rights"： \[  
        「聆聽」，  
        「傳送」  
    \]  
} 與 **New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 一起使用時，上述 JSON 範例會建立一個名為 ContosoAuthorizationRule 的授權規則，提供使用者對命名空間的聆聽和傳送許可權。
用來 *驗證* 的主鍵，可以使用下列 Windows PowerShell 命令隨機產生： \[ 轉換 \] ：：ToBase64String ( (1.32 |% { \[ byte/] (Get-Random -Minimum 0 -最大值 255) }) ) 

## 例子

### 範例 1：建立授權規則並指派給命名空間
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

此命令會建立授權規則，並將該規則指派給命名空間 ContosoNamespace。
建立此規則時，您必須指定適當的命名空間，以及命名空間指派給的資源群組。
不過，您不需要指定規則本身的任何相關資訊：規則資訊會取自輸入C:\Configuration\NamespaceAuthorizationRules.js中。

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

### -InputFile
指定 JSON 檔案的路徑，其中包含新授權規則的組程資訊。

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -命名空間
指定指派授權規則的命名空間。
命名空間提供將通知中樞分組和分類的方式。
新規則必須指派給現有的命名空間。
**New-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 無法建立新命名空間。

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
您必須使用現有的資源群組。
此 Cmdlet 無法建立新資源群組。

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

### -SASRule
指定 **SharedAccessAuthorizationRuleAttributes** 物件，其中包含新規則的組定資訊。

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.SharedAccessAuthorizationRuleAttributes

## 筆記

## 相關連結

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


