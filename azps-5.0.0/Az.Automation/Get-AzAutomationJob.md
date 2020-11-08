---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140566"
---
# Get-AzAutomationJob

## 摘要
取得自動化 runbook 作業。

## 句法

### ByAll (預設) 
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByJobId
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzAutomationJob** Cmdlet 會取得 Azure 自動化中的 runbook 作業。

## 示例

### 範例1：取得特定的 runbook 作業
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

這個命令會取得具有指定 GUID 的作業。

### 範例2：取得 runbook 的所有作業
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

這個命令會取得與名為 Runbook02 的 runbook 相關聯的所有作業。

### 範例3：取得所有執行中的作業
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

這個命令會取得自動帳戶（名為 Contoso17）中所有執行中的作業。

## 參數

### -AutomationAccountName
指定此 Cmdlet 取得作業之自動化帳戶的名稱。

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
將作業的結束時間指定為 **DateTimeOffset** 物件。
您可以指定可轉換成有效 **DateTimeOffset** 的字串。
這個 Cmdlet 會取得在此參數指定的值上或之前有結束時間的作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定此 Cmdlet 所取得作業的識別碼。

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定此 Cmdlet 在其中取得作業的資源群組的名稱。

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

### -RunbookName
指定此 Cmdlet 取得作業的 runbook 名稱。

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
將作業的開始時間指定為 **DateTimeOffset** 物件。
這個 Cmdlet 會取得在此參數指定的值或其之後有開始時間的作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定工作的狀態。
這個 Cmdlet 會取得狀態與此參數相符的作業。
有效值為： 
- 啟用
- 完畢
- 成功
- 排
- 開始
- 進行
- 入門
- 被
- 終止
- 封存
- 封存

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### Guid.empty

### System.object

## 輸出

### [作為] 的 [自動化] 工作

## 筆記

## 相關連結

[AzAutomationJobOutput](./Get-AzAutomationJobOutput.md)

[Resume-AzAutomationJob](./Resume-AzAutomationJob.md)

[停止 AzAutomationJob](./Stop-AzAutomationJob.md)

[暫停-AzAutomationJob](./Suspend-AzAutomationJob.md)


