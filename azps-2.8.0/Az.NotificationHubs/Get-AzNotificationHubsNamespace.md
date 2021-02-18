---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 5c5517faa5dbd65cc6a76a02209cb2b8c429300a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410475"
---
# Get-AzNotificationHubsNamespace

## 簡介
獲得通知中樞命名空間相關資訊。

## 語法

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzNotificationHubsNamespace** Cmdlet 會取得通知中樞命名空間相關資訊。
此 Cmdlet 提供您取得所有命名空間資訊、指派給指定資源群組之命名空間相關資訊的選項;或用於退回特定命名空間的資訊。
命名空間是邏輯容器，可協助組織及管理通知中樞。
您至少必須有一個通知中樞命名空間：所有通知中樞都必須指派給命名空間。
單一命名空間可以包含多個中樞，這表示您可能只需要貴組織的一個命名空間。
不過，您也可以有多個命名空間，以更有效地組織中樞，或給予特定人員管理所選中樞子集的許可權。
**Get-AzNotificationHubsNamespace** Cmdlet 會返回命名空間本身的基本資訊。
若要取得與命名空間相關聯的授權規則相關資訊，請使用 Get-AzNotificationHubsNamespaceAuthorizationRules。

## 例子

### 範例 1：取得所有通知中樞命名空間的資訊
```
PS C:\>Get-AzNotificationHubsNamespace
```

此命令會針對您所有的通知中樞命名空間，會返回資訊。

### 範例 2：取得單一通知中樞命名空間的資訊
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

此命令會獲得單一通知中樞命名空間的資訊：ContosoNamespace。

### 範例 3：取得指派給特定命名空間之所有通知中樞的資訊
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

此命令會獲得指派給資源群組 ContosoNotificationsGroup 的所有通知中樞命名空間的資訊。

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

### -命名空間
指定命名空間的唯一名稱。
命名空間提供將通知中樞分組和分類的方式。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.NotificationHubs.models.命名空間Attributes

## 筆記

## 相關連結


[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


