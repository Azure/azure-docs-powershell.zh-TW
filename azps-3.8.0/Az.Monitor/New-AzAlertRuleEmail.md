---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411359"
---
# New-AzAlertRuleEmail

## 簡介
為警示規則建立電子郵件動作。

## 語法

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzAlertRuleEmail** Cmdlet 會為警示規則建立電子郵件動作。

## 例子

### 範例 1：為服務擁有者建立提醒規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

此命令會建立警示規則電子郵件動作，以在警示規則發出時傳送給服務擁有者。

### 範例 2：為非服務擁有者建立提醒規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

此命令會針對指定的電子郵件地址建立提醒規則電子郵件動作，但服務擁有者則不在此。

### 範例 3：為服務擁有者和非服務擁有者建立提醒規則電子郵件動作
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

此命令會針對指定位址及其服務擁有者建立警示規則電子郵件動作。

## 參數

### -CustomEmail
指定逗號分隔電子郵件地址的清單。

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

### -SendToServiceOwner
表示此作業在規則啟用時傳送電子郵件給服務擁有者。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String[]

### System.Management.Automation.SwitchParameter

## 輸出

### Microsoft.Azure.management.Monitor.management.models.RuleEmailAction

## 筆記

## 相關連結


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWeb一體式](./New-AzAlertRuleWebhook.md)


