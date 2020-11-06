---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450322"
---
# Publish-AzureRmAutomationRunbook

## 摘要
發佈 runbook。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationRunbook** Cmdlet 發佈 runbook，以用於 Azure 自動化的生產環境。

## 示例

### 範例1：發佈 runbook
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

這個命令會在名為 Contoso17 的 Azure 自動化帳戶中發佈名為 Runbk01 的 runbook。

## 參數

### -AutomationAccountName
指定此 Cmdlet 發佈 runbook 的自動化帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 發佈的 runbook 名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 發佈 runbook 的資源群組的名稱。

```yaml
Type: System.String
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

### System.object

## 輸出

### [-Azure. 命令介面]。

## 筆記

## 相關連結

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[匯入-AzureRmAutomationRunbook](./Import-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[新-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[移除-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)

[開始-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)


