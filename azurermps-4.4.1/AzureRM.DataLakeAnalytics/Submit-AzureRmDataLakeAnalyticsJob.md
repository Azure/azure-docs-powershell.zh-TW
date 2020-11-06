---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451724"
---
# Submit-AzureRmDataLakeAnalyticsJob

## 摘要
提交作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 含雙 SQL 腳本路徑的提交作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 提交 U-SQL 作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 含有含 reucurrence 資訊之雙 SQL 腳本路徑的提交作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 使用定期資訊提交 U-SQL 作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 使用含有 reucurrence 和管線資訊的雙 SQL 腳本路徑提交作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 使用週期及管線資訊提交 U-SQL 作業
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmDataLakeAnalyticsJob** Cmdlet 會提交 Azure Data Lake Analytics 作業。

## 示例

### 範例1：提交作業
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

這個命令會提交資料 Lake Analytics 作業。

## 參數

### -帳戶
指定 Data Lake Analytics 帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileMode
指定作業的編譯模式。
此參數可接受的值為：

- 語義
- 填
- SingleBox

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompileOnly
表示此 Cmdlet 編譯作業而不執行它。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DegreeOfParallelism
指定作業的資料 Lake Analytics 單位 (DLAU) ，指出作業允許的最大並行度。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定作業名稱。

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

### -PipelineId
代表此作業提交的識別碼，是一組週期性作業的一部分，也是與作業管線相關聯。

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineName
與此工作相關聯之管線的選擇性易記名稱。

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineUri
連結至與此管線關聯之來源服務的可選 uri。

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -優先順序
指定作業的優先順序。
如果未指定，優先順序為1000。
較低的數位表示較高的作業優先順序。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
代表此作業提交的識別碼，是一組具有相同週期 ID 的週期性作業的一部分。

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceName
作業間定期關聯的選擇性易記名稱。

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RunId
識別管線的此特定執行小程式的識別碼。

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -執行時間
指定作業的執行時間版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -腳本
指定要執行的腳本內容。

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ScriptPath
指定要執行之腳本的本機檔案路徑。

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
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
形參 "Script" 接受來自管線的 "String" 類型的值

## 輸出

### JobInformation
已提交作業的初始作業詳細資料。

## 筆記

## 相關連結

[AzureRmDataLakeAnalyticsJob](./Get-AzureRmDataLakeAnalyticsJob.md)

[停止 AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[稍候-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


