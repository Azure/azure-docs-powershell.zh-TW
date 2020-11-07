---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967757"
---
# Get-AzureSchedulerJob

## 摘要
取得排程作業或特定排程作業的清單。

## 句法

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureSchedulerJobCollection** Cmdlet 會取得排程作業或特定排程作業的清單。

## 示例

### 範例1：取得集合中的所有工作
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

這個命令會取得作業集合中名為 JobCollection01 的排程作業。

### 範例2：取得已命名的工作
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

這個命令會從指定位置中名為 JobCollection01 的集合中取得名為 Job01 的作業。

### 範例3：在集合中取得停用的工作
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

這個命令會在指定位置中取得屬於 JobCollection01 的所有停用排程作業。

## 參數

### -JobCollectionName
指定包含要取得之排程作業的集合的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobName
指定要取得的排程作業名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobState
指定要取得的排程作業狀態。
此參數可接受的值為：

- 後
- 禁止
- 錯誤
- 完畢

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定託管雲端服務的位置名稱。
此參數可接受的值為：

- 亞洲任何地方
- 歐洲任何地方
- 美國任何地方
- 東亞
- 東美國
- 美國中北部
- 北歐
- 美國中南部
- 東南亞
- 西歐
- 美國西部

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## 輸出

## 筆記

## 相關連結

[移除-AzureSchedulerJob](./Remove-AzureSchedulerJob.md)


