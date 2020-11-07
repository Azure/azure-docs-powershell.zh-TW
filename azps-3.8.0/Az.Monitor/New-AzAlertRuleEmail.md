---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958924"
---
# New-AzAlertRuleEmail

## 摘要
建立警示規則的電子郵件動作。

## 句法

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**新的-AzAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。

## 示例

### 範例1：建立服務擁有者的警示規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

當觸發警示規則時，這個命令會建立一個要傳送給其服務擁有者的警示規則電子郵件動作。

### 範例2：為非服務擁有者建立警示規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

這個命令會針對指定的電子郵件地址建立一個警示規則電子郵件動作，但不適用於服務擁有者。

### 範例3：為服務擁有者和非服務擁有者建立警示規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

這個命令會針對指定的位址和其服務擁有者建立一個警示規則電子郵件動作。

## 參數

### -CustomEmail
指定逗號分隔的電子郵件地址清單。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SendToServiceOwner
表示此操作會在規則激發時傳送電子郵件給服務擁有者。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object []

### SwitchParameter 的系統管理功能

## 輸出

### RuleEmailAction 中的 [管理模型]。

## 筆記

## 相關連結

[附加 AzLogAlertRule](./Add-AzLogAlertRule.md)

[附加 AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[附加 AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[新-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


