---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 622b25a4cd84fcdd6ffb8179b3990ac786733e06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911761"
---
# Get-AzBatchSubtask

## 簡介
獲得指定任務的子任務資訊。

## 語法

### ODataFilter (預設) 
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzBatchSubtask** Cmdlet 會取得指定工作之子任務資訊。
子任務可提供個別任務的平行處理，並啟用任務執行與進度的精確監控。

## 例子

### 範例 1：針對指定任務返回所有子任務
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

這些命令會以 ID myTask 來返回工作的所有子任務。
若要這麼做，範例中的第一個命令會建立批次帳戶 contosobatchaccount 帳戶金鑰的物件參照。
此物件參照會儲存在名為 $coNtext 的$coNtext。
接著，第二個命令會使用該物件參照和 **Get-AzBatchSubtask** Cmdlet，以返回 myTask 的所有子任務，此工作會做為 Job-01 的一部分執行。

## 參數

### -BatchCoNtext
指定此 Cmdlet 用來與批次處理服務互動的 **BatchAccountCoNtext** 實例。
如果您使用 Get-AzBatchAccount Cmdlet 取得 BatchAccountCoNtext，則與批次處理服務互動時，將會使用 Azure Active Directory 驗證。 若要改為使用共用金鑰驗證，請使用 Get-AzBatchAccountKey Cmdlet 取得已填入便捷鍵的 BatchAccountCoNtext 物件。 使用共用金鑰驗證時，預設會使用主便捷鍵。 若要變更使用的金鑰，請設定 BatchAccountCoNtext.KeyInUse 屬性。

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
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -JobId
指定包含此 Cmdlet 子任務之工作的工作的識別碼。

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxCount
指定要退回的子任務數上限。
如果您將值指定為 0 (0) ，Cmdlet 不會使用上限。
預設值為 1000。

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

### -工作
指定包含此 Cmdlet 所返回之子任務之工作的物件參照。
此物件參照是使用 Cmdlet Get-AzBatchTask將所返回的物件儲存于變數中來建立。

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskId
指定此 Cmdlet 會返回其子任務的工作識別碼。

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### Microsoft.Azure.Commands.Batch。Models.PSCloudTask

### Microsoft.Azure.Commands.Batch.BatchAccountCoNtext

## 輸出

### Microsoft.Azure.Commands.Batch。Models.PSSubtaskInformation

## 筆記

## 相關連結

[Get-AzBatchTask](./Get-AzBatchTask.md)


