---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138816"
---
# New-AzImportExportDriveListObject

## 摘要
建立 ImportExport 的 DriverList 物件。

## 句法

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## 說明
建立 ImportExport 的 DriverList 物件。

## 示例

### 範例1：為 ImportExport 作業建立新的 DriveList
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

這些 Cmdlet 會為 ImportExport 作業建立新的 DriveList。

## 參數

### -BitLockerKey
用來加密磁片磁碟機的 BitLocker 金鑰。

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

### -BytesSucceeded
已成功地傳送磁片磁碟機的位元組數。

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CopyStatus
資料傳輸處理常式的詳細狀態。
除非磁碟機處於轉移狀態，否則不會在回應中傳回此欄位。

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

### -DriveHeaderHash
磁片磁碟機標頭雜湊值。

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

### -DriveId
磁碟機的硬體序列值（不含空格）。

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

### -ErrorLogUri
指向內含資料傳送操作之錯誤記錄的 blob 的 URI。

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

### -ManifestFile
磁碟機上資訊清單檔案的相對路徑。

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

### -ManifestHash
磁片磁碟機上的資訊清單檔案的 Base16 編碼 MD5 雜湊值。

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

### -ManifestUri
指向內含磁片磁碟機資訊清單檔案之 blob 的 URI。

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

### -百分比
已完成磁片磁碟機的百分比。

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

### -State
磁片磁碟機的目前狀態。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VerboseLogUri
指向內含資料傳輸作業詳細資料記錄之 blob 的 URI。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### IDriveStatus （ImportExport）。 Api20161101。

## 筆記

別名

## 相關連結

