---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: b3484b410ef885567010c05660590808f3995308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449356"
---
# New-AzureRmAlertRuleEmail

## 摘要
建立警示規則的電子郵件動作。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzureRmAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。

## 示例

### 範例1：建立服務擁有者的警示規則電子郵件動作
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

當觸發警示規則時，這個命令會建立一個要傳送給其服務擁有者的警示規則電子郵件動作。

### 範例2：為非服務擁有者建立警示規則電子郵件動作
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

這個命令會針對指定的電子郵件地址建立一個警示規則電子郵件動作，但不適用於服務擁有者。

### 範例3：為服務擁有者和非服務擁有者建立警示規則電子郵件動作
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

這個命令會針對指定的位址和其服務擁有者建立一個警示規則電子郵件動作。

## 參數

### -CustomEmail
指定逗號分隔的電子郵件地址清單。

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 0
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

### -SendToServiceOwner
表示此操作會在規則激發時傳送電子郵件給服務擁有者。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendToServiceOwners

Required: False
Position: Named
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

### RuleEmailAction 中的 [管理模型]。

## 筆記

## 相關連結

[附加 AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[附加 AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[附加 AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[新-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


