---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967817"
---
# Get-AzureAutomationAccount

## 摘要

取得 Azure 自動化帳戶。

## 句法

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**AzureAutomationAccount** Cmdlet 會為您的訂閱取得 Microsoft Azure 自動化帳戶。
自動化帳戶是與其他自動化帳戶資源隔離的自動化資源容器。
自動化資源包括 runbook、工作和資產。

## 示例

### 範例1：取得自動化帳戶
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

這個命令會取得名為 Contoso17 的自動化帳戶。

## 參數

### -位置
指定與自動化帳戶相關聯的 Azure 位置。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定 Azure 自動化帳戶的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

### AutomationAccount 中的 [.]

## 筆記

## 相關連結

[新-AzureAutomationAccount](./New-AzureAutomationAccount.md)

[移除-AzureAutomationAccount](./Remove-AzureAutomationAccount.md)


