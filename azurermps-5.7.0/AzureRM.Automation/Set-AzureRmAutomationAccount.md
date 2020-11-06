---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: bbb90e728c9c43c011c4610ee47273af1fdae668
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450731"
---
# Set-AzureRmAutomationAccount

## 摘要
修改自動化帳戶。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationAccount** Cmdlet 會修改 Azure 自動化帳戶。

如需自動化帳戶的詳細資訊，請參閱 New-AzureRmAutomationAccount Cmdlet。

## 示例

### 範例1：設定自動化帳戶的標記
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

第一個命令會將兩個鍵/值對指派給 $Tags 變數。

第二個命令會在 $Tags 中為名為 AutomationAccount01 的自動化帳戶設定標記。

### 範例2：變更自動化帳戶的方案
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

這個命令會將計畫變更為基本的自動化帳戶（名為 AutomationAccount01）。

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

### -名稱
指定此 Cmdlet 所修改之自動化帳戶的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -方案
指定自動化帳戶的方案。
有效值為：

- 空白
- 空閒

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含此 Cmdlet 所修改之自動化帳戶的資源群組的名稱。

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

### -標記
雜湊資料表形式的索引鍵/值對。 例如：

@ {key0 = "value0"; key1 = $null; key2 = "value2"}

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

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

### AutomationAccount 中的 [.]

## 筆記

## 相關連結

[AzureRmAutomationAccount](./Get-AzureRmAutomationAccount.md)

[新-AzureRmAutomationAccount](./New-AzureRmAutomationAccount.md)

[移除-AzureRmAutomationAccount](./Remove-AzureRmAutomationAccount.md)
