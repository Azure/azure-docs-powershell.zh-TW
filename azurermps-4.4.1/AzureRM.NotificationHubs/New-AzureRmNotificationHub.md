---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: 33dfd5a8c4bde0405351315543078558a5832aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446705"
---
# New-AzureRmNotificationHub

## 摘要
建立通知中樞。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### InputFileParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
**新的-AzureRmNotificationHub** Cmdlet 會建立通知中樞。
通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。
通知中樞大致相當於個別的應用程式：您的每個應用程式通常都有自己的通知中樞。

**新的 AzureRmNotificationHub** Cmdlet 提供兩種方式來建立新的通知中樞。
您可以建立 **NotificationHubAttributes** 物件的實例，然後設定該物件。
然後，您可以透過 *NotificationHubObj* 參數，將這些屬性值複製到新的中樞。

或者，您也可以建立 JSON (JavaScript 物件符號) 檔案，其中包含相關的配置值，然後使用 *InputFile* 參數套用這些值。

當與 **AzureRmNotificationHub** Cmdlet 搭配使用時，前面的 JSON 範例會建立名為 ContosoNotificationHub 的通知中心，該中樞位於美國西部資料中心。

## 示例

### 範例1：建立通知中樞
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

這個命令會在命名空間 ContosoNamespace 中建立通知中樞。
新的中樞會指派給 ContosoNotificationsGroup。
您不需要為中樞指定名稱或任何其他配置資訊;該資訊將會從 C:\Configurations\InternalHub.js的輸入檔案中取得。

## 參數

### -InputFile
指定 JSON 檔案的路徑，該檔案包含新通知中樞的配置值。

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
指定要將通知中心指派給哪個命名空間。

命名空間提供一種群組和分類通知中樞的方式。
通知中樞必須指派給現有的命名空間。
**新的-AzureRmNotificationHub** Cmdlet 無法建立新的命名空間。

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
指定包含新中樞之配置資訊的 **NotificationHubAttributes** 物件。

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
指定要將通知中心指派給哪個資源群組。
資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。

您必須使用現有的資源群組。
**新的-AzureRmNotificationHub** Cmdlet 無法建立新的資源群組。

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

[移除-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


