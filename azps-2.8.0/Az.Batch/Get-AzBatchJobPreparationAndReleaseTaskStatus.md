---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobpreparationandreleasetaskstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobPreparationAndReleaseTaskStatus.md
ms.openlocfilehash: accba78cd05d6fcc18eb7f48c7cfb2839c0e9417
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799370"
---
# Get-AzBatchJobPreparationAndReleaseTaskStatus

## 摘要
取得批次工作準備與發行任務狀態。

## 句法

### 識別碼 (預設) 
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-Id] <String> [-Filter <String>] [-MaxCount <Int32>]
 [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchJobPreparationAndReleaseTaskStatus [-InputObject] <PSCloudJob> [-Filter <String>]
 [-MaxCount <Int32>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzBatchJobPreparationAndReleaseTaskStatus** Cmdlet 會取得批次作業的 Azure Batch 作業準備與釋放工作狀態。
您必須將 *識別碼* 參數或 **PSCloudJob** 實例提供給這個 Cmdlet。

## 示例

### 範例1：取得工作的工作準備與發行狀態
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $Context -Id Test

ComputeNodeId                          : tvm-2316545714_1-20170613t201733z
ComputeNodeUrl                         : https://account.westus.batch.azure.com/pools/test/nodes/tvm-2316545714_1-20170613t201733z
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 : test
```

這個命令會取得作業「Test」的工作準備與發行任務狀態。
使用 Get-AzBatchAccountKeys Cmdlet 將內容指派給 $CoNtext 變數。

### 範例2：使用篩選來取得工作的工作準備與發行狀態，並選取 [已指定]
```
PS C:\> Get-AzBatchJobPreparationAndReleaseTaskStatus -BatchContext $context -Id Test -Filter "nodeId eq 'tvm-2316545714_1-20170613t201733z'" -Select "jobPreparationTaskExecutionInfo"

ComputeNodeId                          :
ComputeNodeUrl                         :
JobPreparationTaskExecutionInformation : Microsoft.Azure.Commands.Batch.Models.PSJobPreparationTaskExecutionInformation
JobReleaseTaskExecutionInformation     :
PoolId                                 :
```

這個命令會在節點「tvm-2316545714_1-20170613t201733z」上取得作業「Test」的工作準備與發行任務狀態，並使用 Select 子句指定僅傳回 JobPreparationTaskExecutionInformation 資訊

## 參數

### -BatchCoNtext
與批次服務互動時要使用的 BatchAccountCoNtext 實例。
使用 Get-AzBatchAccountKeys Cmdlet 來取得已填入其便捷鍵的 BatchAccountCoNtext 物件。

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -展開
指定 (OData) expand 子句中的開放式資料通訊協定。
指定此參數的值，以取得您所取得之主要實體的關聯實體。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -篩選
指定 OData 篩選子句。
如果您沒有指定篩選，此 Cmdlet 會傳回作業的所有工作準備與發行任務狀態。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定要檢索其準備與發行工作的作業識別碼。
您無法指定通配字元。

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
指定代表作業的 **PSCloudJob** 物件，以取得準備與發行任務狀態。
若要取得 **PSCloudJob** 物件，請使用 Get-AzBatchJob Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJob
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxCount
指定要傳回的工作準備與發行任務狀態的數目上限。
如果您指定的值為零 (0) 或更小，則 Cmdlet 不會使用上限。
預設值為1000。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -選取
指定 OData select 子句。
指定此參數的值，以取得特定屬性，而不是所有物件屬性。

```yaml
Type: System.String
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

### Microsoft.Azure.Commands.Batch。PSCloudJob

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### Microsoft.Azure.Commands.Batch。PSJobPreparationAndReleaseTaskExecutionInformation

## 筆記

## 相關連結

[AzBatchJob](./Get-AzBatchJob.md)

[Azure 批次 Cmdlet](/powershell/module/az.batch)
