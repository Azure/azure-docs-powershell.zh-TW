---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 02e0678b9c86643df9cd4bfc2192908ed4748249
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439372"
---
# Get-AzDataLakeAnalyticsJob

## 摘要
取得資料 Lake Analytics 作業。

## 句法

### GetAllInResourceGroupAndAccount (預設) 
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobInformation
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzDataLakeAnalyticsJob** Cmdlet 會取得 Azure Data Lake Analytics 作業。
如果您沒有指定作業，此 Cmdlet 會取得所有作業。

## 示例

### 範例1：取得指定的工作
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

這個命令會取得具有指定識別碼的作業。

### 範例2：取得上周提交的工作
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

此命令會取得上周提交的工作。

## 參數

### -帳戶
指定資料 Lake Analytics 帳戶的名稱。

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

### -包含
指定選項，以指示要取得工作的其他資訊類型。
此參數可接受的值為：
- 所有
- DebugInfo
- Statistics
- 同時

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -作業 Id
指定要取得的作業識別碼。

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -名稱
指定要用來篩選工作清單結果的名稱。
此參數可接受的值為：
- 所有
- DebugInfo
- Statistics
- 同時

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
一個選用的識別碼，只指示應傳回指定管線的工作部分。

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
一個選用的識別碼，只指示應該傳回指定的定期作業部分。

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -結果
指定作業結果的結果篩選器。
此參數可接受的值為：
- 所有
- 取消
- 成功
- 成功

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
指定作業結果的狀態篩選器。
此參數可接受的值為：
- 認可
- 新增功能
- 編譯
- 排程
- 排
- 入門
- 處於
- 進行
- 截至

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
指定日期篩選。
使用此參數可將作業清單結果篩選為在指定日期之後提交的作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
指定日期篩選。
使用此參數可將作業清單結果篩選為在指定日期前提交的作業。

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -提交者
指定使用者的電子郵件地址。
使用此參數可將作業清單結果篩選為指定使用者所提交的工作。

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -上方
指明要傳回的作業數的選用值。 預設值為500

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### Guid.empty

### DataLakeAnalyticsEnums + ExtendedJobData （DataLakeAnalytics）。

### "CoreLib" 1 [（System.object，System.object，，版本 = 4.0.0.0，Culture = 中立，

### JobState [] DataLake. []

### JobResult [] DataLake. []

### "CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]

### "CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]

## 輸出

### [DataLake. JobInformation]。

## 筆記

## 相關連結

[停止 AzDataLakeAnalyticsJob](./Stop-AzDataLakeAnalyticsJob.md)

[Submit-AzDataLakeAnalyticsJob](./Submit-AzDataLakeAnalyticsJob.md)

[稍候-AzDataLakeAnalyticsJob](./Wait-AzDataLakeAnalyticsJob.md)


