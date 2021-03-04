---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 30c6a16d7b9cfb94f1fb2032940aa4587d27e550
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901698"
---
# Set-AzNotificationHubAuthorizationRule

## 簡介
設定通知中樞的授權規則。

## 語法

### InputFileParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Set-AzNotificationHubAuthorizationRule** Cmdlet 會修改指派給通知中樞的共用存取簽名 (SAS) 授權規則。
授權規則會依據不同的許可權等級，建立連結做為 URI 來管理通知中樞的存取權。
許可權等級可以是下列其中一項： 
- 聽
- 發送
- 管理用戶端會依據適當的許可權等級，導向至其中一個 URI。
例如，提供聆聽許可權的用戶端會導向至該許可權的 URI。
此 Cmdlet 提供兩種方式來修改指派給通知中樞的授權規則。
例如，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後將該物件設定為您想要規則擁有的屬性值。
您可以透過 .NET Framework 設定物件。
接著，您可以使用 *SASRule* 參數，將那些屬性值複製到規則。
或者，您可以建立 JSON (JavaScript 物件表示) 包含相關組設定值的檔案，然後透過 *InputFile* 參數來使用這些值。
JSON 檔案是使用類似以下語法的文字檔：{ "Name"： "ContosoAuthorizationRule"，  
  "PrimaryKey"："WE4qH0398AyXjlekt56gg1g VM3NHoMs29KkUnnpUk01Y="，  
  "Rights"： \[  
        「聆聽」，  
        「傳送」  
    \]  
  } 與 New-AzNotificationHubAuthorizationRule Cmdlet 一起使用時，上述 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，以便讓使用者擁有中樞的聆聽和傳送許可權。

## 例子

### 範例 1：修改指派給通知中樞的授權規則
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

此命令會修改指派給 ContosoExternalHub 通知中樞的授權規則。
您必須指定中樞所在的命名空間，以及指派中樞的資源群組。
已修改規則的資訊不會包含在命令本身中。
相反地，該資訊會位於您C:\Configuration\AuthorizationRules.js檔案中。

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

### -InputFile
指定 JSON 檔案的路徑，其中包含新規則的組程資訊。

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
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
通知中樞可用來傳送推入通知給多個用戶端，而不管這些用戶端使用什麼。

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
指定指派通知中樞給的資源群組。 資源群組會以只協助庫存管理和 Azure 系統管理的方式整理專案，例如命名空間、通知中樞和授權規則。

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
指定 **SharedAccessAuthorizationRuleAttributes** 物件，該物件包含已修改之授權規則的組定資訊。

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
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

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)


