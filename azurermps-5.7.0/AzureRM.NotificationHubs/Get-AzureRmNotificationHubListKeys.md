---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhublistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 49bb03e903d465b372bc00118e15369f158661e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449266"
---
# Get-AzureRmNotificationHubListKeys

## 摘要
取得與通知中樞授權規則相關聯的主要和次要連接字串。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubListKeys** Cmdlet 會傳回通知中樞共用存取簽章的主要和次要連接字串， (SAS) 授權規則。

授權規則可管理使用者對中心的許可權。
每個規則都包含主要和次要的連線字串。
這些連接字串 (Uri) 執行下列動作：

- 將使用者指向資源。
- 包含含查詢參數的權杖。

其中一個參數（即簽名）是用來驗證使用者，並提供指定的存取層級。

## 示例

### 範例1：取得授權規則的主要和次要連接字串
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

這個命令會取得授權規則 ListenRule （指派給 ContosoInternalHub 通知中樞的規則）的主要和次要連接字串。
命令必須包含中樞命名空間和資源群組。

## 參數

### -AuthorizationRule
指定 (SAS) 驗證規則的共用存取簽章名稱。
這些規則決定使用者對通知中樞所擁有的存取類型。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -命名空間
指定通知中心指派給哪個命名空間。

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

### -NotificationHub
指定此 Cmdlet 指派授權規則的通知中樞。
通知中樞可用來傳送推播通知給多個用戶端，而不管這些用戶端使用的平臺為何。

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

### -ResourceGroup
指定通知中心指派給哪個資源群組。
資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

### ResourceListKeys 中的 NotificationHubs。

## 筆記

## 相關連結

[AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)


