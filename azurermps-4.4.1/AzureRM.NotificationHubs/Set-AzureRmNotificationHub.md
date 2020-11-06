---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: 45e61b79381cc9acddf4dc12c5d8e905627130a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448076"
---
# Set-AzureRmNotificationHub

## 摘要
設定通知中樞的屬性值。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### InputFileParameterSet
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHub** Cmdlet 會修改通知中樞的屬性值。

您可以透過兩種方式來修改通知中樞屬性值。
若是一個，您可以建立 **NotificationHubAttributes** 物件的實例，然後使用您想要新的中樞擁有的屬性值來設定該物件。
這可以透過 .NET 架構來完成。
然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到您的中樞。

或者，您也可以建立包含相關設定值) 檔案的 JSON (JavaScript 物件符號，然後透過 *InputFile* 參數套用這些值。
JSON 檔案是一個文字檔，該檔案使用類似下列的語法：

{  
    "Name"： "ContosoNotificationHub"，  
    "位置"： "西 US"，  
}

當與 **AzureRmNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會將名為 ContosoNotificationHub 之通知中樞的 Location 值設為 [西部]。

## 示例

### 範例1：修改通知中樞的屬性值
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

這個命令會修改在 ContosoNamespace 命名空間中找到之通知中心的屬性值，並將其指派給資源群組 ContosoNotificationsGroup。
在命令中不會指定屬性值，以及要修改之中樞的名稱。
相反地，該資訊會包含在 C:\Configuration\Hubs.js的輸入檔案中。

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
指定包含通知中樞配置資訊的 JSON 檔案路徑。

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

### -NotificationHubObj
指定包含此 Cmdlet 所修改之中樞之配置資訊的 **NotificationHubAttributes** 物件。

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
指定通知中心指派給哪個資源群組。
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

### NotificationHubAttributes 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHub](./Get-AzureRmNotificationHub.md)

[新-AzureRmNotificationHub](./New-AzureRmNotificationHub.md)

[移除-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)


