---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 996904a68e8cb55aa4964a6c776064722c63dbab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449262"
---
# Get-AzureRmNotificationHubsNamespace

## 摘要
取得通知中心命名空間的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmNotificationHubsNamespace** Cmdlet 會取得通知中心命名空間的相關資訊。
這個 Cmdlet 可讓您選擇取得所有命名空間的資訊，以及指派給指定資源群組的命名空間資訊;或傳回特定命名空間的相關資訊。

命名空間是邏輯容器，可協助您組織和管理通知中樞。
您必須至少有一個通知中心命名空間：所有通知中樞都必須指派給命名空間。
單一命名空間可以存放多個中心，這表示您在組織中可能只需要一個命名空間。
不過，您也可以使用多個命名空間來更完善地組織您的中樞，或提供特定的個人許可權來管理選取的中樞子集。

**AzureRmNotificationHubsNamespace** Cmdlet 會傳回有關命名空間本身的基本資訊。
若要取得與命名空間相關聯之授權規則的相關資訊，請使用 AzureRmNotificationHubsNamespaceAuthorizationRules。

## 示例

### 範例1：取得所有通知中心命名空間的相關資訊
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

這個命令會傳回所有通知中心命名空間的資訊。

### 範例2：取得單一通知中樞命名空間的相關資訊
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

這個命令會取得單一通知中樞命名空間的資訊： ContosoNamespace。

### 範例3：取得指派給特定命名空間之所有通知中心的相關資訊
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

這個命令會取得指派給資源群組 ContosoNotificationsGroup 的所有通知中心命名空間的資訊。

## 參數

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
指定命名空間的唯一名稱。

命名空間提供一種群組和分類通知中樞的方式。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
指定將命名空間指派給哪個資源群組。

資源群組會以協助您簡單地清查管理和 Azure 管理的方式，來組織諸如命名空間、通知中樞和授權規則等專案。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### [System.object]. 清單 ' 1 [NotificationHubs]。 NamespaceAttributes]

## 筆記

## 相關連結

[AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[新-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[移除-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


