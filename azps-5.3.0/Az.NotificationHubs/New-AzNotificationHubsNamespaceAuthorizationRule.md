---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436285"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## 摘要
建立授權規則，並將該規則指派給通知中心命名空間。

## 句法

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

## 說明
**新的-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 會 (SAS) 授權規則建立共用的存取簽章，並將它指派給通知中心命名空間。
授權規則會管理使用者權利，以及該命名空間所含的通知中心。
這個 Cmdlet 提供兩種方式來建立新的授權規則，並將它指派給命名空間。
您可以建立 **SharedAccessAuthorizationRuleAttributes** 物件的實例，然後使用您想要新規則擁有的屬性值來設定該物件。
這可以使用 .NET Framework 來完成。
然後，您可以使用 *SASRule* 參數，將這些屬性值複製到您的新規則。
或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後使用 *InputFile* 參數套用這些值。
JSON 檔案是一個文字檔，該檔案使用類似下列的語法： {  
    "Name"： "ContosoAuthorizationRule"，  
    "PrimaryKey"： "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y ="，  
    "版權"： \[  
        [聆聽]，  
        收發  
    \]  
} 與 **新的-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 搭配使用時，前面的 JSON 範例會建立名為 ContosoAuthorizationRule 的授權規則，讓使用者聆聽並傳送該命名空間的許可權。
使用下列 Windows PowerShell 命令時，可以隨機產生用於驗證的 *PrimaryKey* ： \[ Convert \] ：： ToBase64String ( # B1 1. 32 |% { \[ Byte/] (取得最小值-最小值 0-最高 255) } ) # A5

## 示例

### 範例1：建立授權規則並將它指派給命名空間
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

這個命令會建立授權規則，並將該規則指派給命名空間 ContosoNamespace。
建立此規則時，您必須指定適當的命名空間和命名空間所指派的資源群組。
不過，您不需要指定規則本身的任何相關資訊：將會從輸入檔案中取得規則資訊 C:\Configuration\NamespaceAuthorizationRules.js[開啟]。

## 參數

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

### -InputFile
指定包含新授權規則之配置資訊的 JSON 檔案路徑。

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
指定將指派授權規則的命名空間。
命名空間提供一種群組和分類通知中樞的方式。
新規則必須指派給現有的命名空間。
**新的-AzNotificationHubsNamespaceAuthorizationRule** Cmdlet 無法建立新的命名空間。

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
您必須使用現有的資源群組。
這個 Cmdlet 無法建立新的資源群組。

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
指定包含新規則之配置資訊的 **SharedAccessAuthorizationRuleAttributes** 物件。

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

## 輸出

### SharedAccessAuthorizationRuleAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[移除-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


