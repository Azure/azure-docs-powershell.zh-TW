---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b6052172ecca2821b1373d93a8de870969a6b4f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915006"
---
# Invoke-AzStorageSyncCompatibilityCheck

## 簡介
檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。

## 語法

### PathBased (預設) 
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## 描述
**Invoke-AzStorageSyncCompatibilityCheck** Cmdlet 會檢查系統與 Azure 檔案同步處理之間潛在的相容性問題。如果為本地或遠端路徑，它會在系統與檔案命名空間上執行一組驗證，然後會返回找到的任何相容性問題。
系統檢查：
- OS 相容性檔案命名空間檢查：
- 不支援的字元
- 檔案大小上限
- 路徑長度上限
- 檔案長度上限
- 資料集大小上限
- 目錄深度上限

## 例子

### 範例 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

此命令會檢查系統以及 C：\DATA 中檔案和資料夾的相容性。

### 範例 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

此命令會檢查 C：\DATA 中檔案和資料夾的相容性，但不執行系統相容性檢查。

### 範例 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

此命令會檢查系統以及 C：\DATA 中檔案和資料夾的相容性，然後將結果匯出為 CSV 檔案至 C：\results。

## 參數

### -ComputerName
您執行此檢查的電腦。

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -認證
您驗證之共用之認證。

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -路徑
您驗證之共用之 UNC 路徑。

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
設定此標號以略過檔案命名空間驗證，只執行系統驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
設定此標號以略過系統驗證，只執行檔案命名空間驗證。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.storageSync.evaluation.models.PSValidationResult

## 筆記
* 關鍵字：azure、Az、arm、resource、management、storagesync、filesync

## 相關連結
