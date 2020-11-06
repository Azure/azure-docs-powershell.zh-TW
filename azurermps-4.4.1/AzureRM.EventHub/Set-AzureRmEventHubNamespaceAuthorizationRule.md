---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457600"
---
# Set-AzureRmEventHubNamespaceAuthorizationRule

## 摘要
更新指定事件中樞命名空間上的授權規則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## 說明
Set-AzureRmEventHubNamespaceAuthorizationRule Cmdlet 會更新指定事件中樞命名空間上的授權規則。

## 示例

### 範例1
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

更新授權規則 \` MyAuthRuleName \` ，以授與管理許可權。

## 參數

### -AuthorizationRuleName
授權規則名稱。
如果未指定-AuthruleObj，則為必要。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuthRuleObj
事件中心命名空間授權規則物件。

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

### -許可權
如果未指定-AuthruleObj，則為必要。
版權例如，@ ( 「聆聽」、「傳送」、「管理」 ) 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## 輸入

### System.object

## 輸出

### SharedAccessAuthorizationRuleAttributes 的 [.]

## 筆記

## 相關連結

