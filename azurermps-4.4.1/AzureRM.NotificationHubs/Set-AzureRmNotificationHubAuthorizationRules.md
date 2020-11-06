---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448078"
---
# Set-AzureRmNotificationHubAuthorizationRules

## 摘要
設定通知中樞的授權規則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### InputFileParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubAuthorizationRules** Cmdlet 會修改指派給通知中樞 (SAS) 授權規則的共用存取簽章。

授權規則會根據不同的許可權等級，以 Uri 來管理通知中樞的存取權。
許可權等級可以是下列其中一項： 

- 聆聽
- 發送
- 管理

用戶端會根據適當的許可權等級，導向到其中一個 Uri。
例如，擁有 [偵聽] 許可權的用戶端將會導向該許可權的 URI。

這個 Cmdlet 提供兩種方式來修改指派給通知中樞的授權規則。
若是一個，您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您希望規則擁有的屬性值來設定該物件。
您可以透過 .NET Framework 來設定物件。
然後，您可以使用 *SASRule* 參數，將這些屬性值複製到規則。

或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後透過 *InputFile* 參數套用這些值。
JSON 檔案是一個文字檔，該檔案使用類似以下的語法：

{"Name"： "ContosoAuthorizationRule"，  
    "PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，  
    "版權"： \[  
        [聆聽]，  
        收發  
    \]  
}

與 New-AzureRmNotificationHubAuthorizationRules Cmdlet 搭配使用時，前面的 JSON 範例會修改名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送許可權給中樞。

## 示例

### 範例1：修改指派給通知中樞的授權規則
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

這個命令會修改指派給名為 ContosoExternalHub 之通知中樞的授權規則。
您必須指定中樞所在的命名空間，以及該中樞指派的資源群組。
在命令本身中不會包含已修改之規則的相關資訊。
相反地，該資訊會在 C:\Configuration\AuthorizationRules.js的輸入檔案中找到。

## 參數

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

### -InputFile
指定包含新規則之配置資訊的 JSON 檔案路徑。

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
通知中心是用來傳送推播通知給多個用戶端，而不考慮這些用戶端的用途。

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
指定通知中心指派給哪個資源群組。 資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。

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
指定包含已修改之授權規則之設定資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。

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

### SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[新-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[移除-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)


