---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationHybridWorkerGroup.md
ms.openlocfilehash: 1f2c82bc51cb5faba9f5b1dd0524e7aced2f0b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452620"
---
# Get-AzureRMAutomationHybridWorkerGroup

## 摘要
取得混合式 runbook 輔助角色群組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByAll (預設) 
```
Get-AzureRMAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRMAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationHybridWorkerGroup** Cmdlet 會取得 Azure 自動化混合式 runbook 輔助角色群組。
若要取得特定群組，請指定其名稱。

## 示例

### 範例1：取得所有混合式 runbook 輔助角色群組
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

這個命令會在自動化帳戶（名為 Contoso17）中取得所有混合式 runbook worker 群組。

### 範例2：取得單一混合式 runbook 輔助角色群組
```
PS C:\>Get-AzureRMAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

這個命令會在自動化帳戶（名為 Contoso17）中取得名為 HybridRunbookWorkerGroup01 的混合式 runbook worker 群組。

### 範例3：在混合式 runbook worker 群組中取得工作人員
```
PS C:\>(Get-AzureRMAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

這個命令會在自動化帳戶（名為 Contoso17）的混合式 runbook worker 群組中取得混合式 runbook 輔助角色。

## 參數

### -AutomationAccountName
指定自動化帳戶的名稱。

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

### -名稱
指定混合式 runbook worker 組名稱。

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 字串
形參 "Name" 接受管線中類型 "String" 的值

## 輸出

### HybridRunbookWorker 中的 [.]

## 筆記

## 相關連結

