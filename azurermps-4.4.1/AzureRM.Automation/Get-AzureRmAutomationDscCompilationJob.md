---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452608"
---
# Get-AzureRmAutomationDscCompilationJob

## 摘要
在自動化中取得 DSC 編譯作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByAll (預設) 
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByJobId
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmAutomationDscCompilationJob** Cmdlet 會在 Azure 自動化中取得 DSC) 編譯作業 (的 Ap 所需狀態設定。

## 示例

### 範例1：取得所有的 DSC 編譯作業
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

這個命令會取得自動帳戶（名為 Contoso17）中的所有編譯作業。

### 範例2：取得設定的 DSC 編譯作業
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

這個命令會針對自動化帳戶（名為 Contoso17）中名為 ContosoConfiguration 的 DSC 配置取得所有編譯作業。

### 範例3：取得特定的 DSC 編譯作業
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

這個命令會取得自動化帳戶（名為 Contoso17）中具有指定識別碼的編譯作業。

## 參數

### -AutomationAccountName
指定包含此 Cmdlet 所取得的 DSC 編譯作業之自動化帳戶的名稱。

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

### -ConfigurationName
指定此 Cmdlet 取得編譯作業的 DSC 配置名稱。

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
指定結束時間。
這個 Cmdlet 會取得已在此參數指定時間開始的編譯作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定此 Cmdlet 取得之 DSC 編譯作業的唯一識別碼。

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
指定此 Cmdlet 取得 DSC 編譯作業之資源群組的名稱。

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

### -StartTime
指定開始時間。
這個 Cmdlet 會取得在此參數指定時間之後或之後開始的作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -狀態
指定此 Cmdlet 取得作業的狀態。
有效值為： 

- 完畢 
- 成功 
- 排 
- 入門 
- 開始 
- 進行 
- 被 
- 終止 
- 封存 
- 封存 
- 啟用
- 新增功能

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

## 輸出

### CompilationJob 中的 [.]

## 筆記

## 相關連結

[AzureRmAutomationDscCompilationJobOutput](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[開始-AzureRmAutomationDscCompilationJob](./Start-AzureRmAutomationDscCompilationJob.md)


