---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966998"
---
# Get-AzureStorSimpleTask

## 摘要
取得 StorSimple 裝置上任務的狀態。

## 句法

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureStorSimpleTask** Cmdlet 會檢索在 Azure StorSimple 裝置上以非同步方式執行的任務狀態。

當您管理 StorSimple 裝置時，大部分的建立、讀取、更新及刪除動作都可以以非同步方式執行。
Windows PowerShell 會傳回 **TaskId** 。
使用識別碼來取得任務的目前狀態。

## 示例

### 範例1：取得任務的狀態
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

這個命令會取得具有指定識別碼之任務的狀態。
結果會顯示任務的狀態為 [已完成]，且結果為 [成功]。

## 參數

### -InstanceId
指定此 Cmdlet 追蹤狀態的任務識別碼。

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### 所有

## 輸出

### JobStatusInfo
這個 Cmdlet 會傳回包含下欄欄位的 **TaskStatusInfo** 物件： 

- **錯誤** 。
**ErrorDetails** ，其中包含程式 **代碼** 和 **訊息** 。
- **TaskId** 。
**字串** 。
傳回其狀態的任務識別碼。
- **TaskSteps** 。
**IList \<TaskStep\>** 。
每個 **TaskStep** 物件都包含 **詳細資料** 、 **ErrorCode** 、 **訊息** 、 **結果** 和 **狀態** 。
- **結果** 。
[ **TaskResult** ]，其中包含任務的整體結果。
有效值為：失敗、成功、PartialSuccess、已取消且無效。
- **狀態** 。
[ **TaskStatus** ]，其中包含任務的整體執行狀態。
有效值為： Inprogress、無效且已完成。
- **TaskResult** 。
**TaskResult** ，根據 **結果** 和 **狀態** 計算出的值。
有效值為：失敗、成功、InProgress、PartialSuccess、已取消且無效。

## 筆記

## 相關連結

