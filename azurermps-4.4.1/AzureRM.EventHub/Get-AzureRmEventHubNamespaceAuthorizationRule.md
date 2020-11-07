---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bad0e86061a5ffaa937209d778d5eaa83e29879d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626302"
---
# Get-AzureRmEventHubNamespaceAuthorizationRule

## 摘要
取得 Eventubs 命名空間授權規則的詳細資料，或取得授權規則清單。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [[-AuthorizationRuleName] <String>]
```

## 說明
Get-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會取得指定事件中樞命名空間授權規則的詳細資料，或命名空間授權規則清單。
如果提供授權規則名稱，則會傳回單一授權規則的詳細資料。
如果未提供授權規則名稱，則會傳回命名空間中的所有授權規則清單。

## 示例

### 範例1
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

傳回 \` \` 事件中心命名空間 MyNamespaceName 中的授權規則 \` MyAuthRuleName \` （含資源群組 \` MyResourceGroupName） \` 。

### 範例2
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName RootManageSharedAccessKey
```

傳回 [ \` \` 事件中心] 命名空間 MyNamespaceName 中的預設授權規則 RootManageSharedAccessKey \` \` ，其中包含 [資源群組 \` MyResourceGroupName] \` 。

### 範例3
```
PS C:\> Get-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

傳回 [事件中心] 命名空間 MyNamespaceName 中的所有授權規則 \` \` ，以及 [資源] 群組 \` MyResourceGroupName \` 。

## 參數

### -AuthorizationRuleName
事件中心命名空間授權規則名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamespaceName
事件中心命名空間名稱。

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

### -ResourceGroupName
資源組名稱。

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

## 輸入

### System.object

## 輸出

### [System.object]。清單 ' 1 [SharedAccessAuthorizationRuleAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））

## 筆記

## 相關連結

